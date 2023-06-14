class Solution {
public:
    string reverseWords(string s) {
        stack<string> st;
        int n=s.size();
        int i=0;
        string ans;
        while(i<n)
        {
            string temp;
            while(i<n && s[i]!=' ')
            {
                temp.push_back(s[i++]);
            }
            if(temp.size()!=0)
            st.push(temp);
            else
            i++;
        }


        
        while(!st.empty())
        {
            ans = ans + st.top();
            st.pop();
            ans.push_back(' ');

        }
        ans.pop_back();
        return ans;
        
    }
};
