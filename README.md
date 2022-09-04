# Deploy Next.js app to Firebase Hosting

1. Upgrade your Firebase project
   1. Go to the Firebase console: https://console.firebase.google.com/
   2. (Create and) open your project
   3. Cog (⚙️) on the sidebar > Usage and billing > Details & settings > Firebase billing plan > Modify plan
   4. Change project's plan from Spark (free) to Blaze (pay as you go)
2. Create a Next.js app: `npx create-next-app@latest --ts`
3. Set up Firebase
   1. Install CLI: `npm install -D firebase-tools`
   2. Set up the project: `npx firebase init hosting`
4. Let Firebase support Next.js
   1. Enable the feature: `npx firebase --open-sesame frameworkawareness`
   2. Replace `"public": "public"` in `firebase.json` with `"source": "."`
   3. (Optional) try local: `npx firebase serve`
5. Deploy: `npx firebase deploy`
6. Open your site: `https://<FB_ID>.web.app`

## References

- [FirebaseExtended/firebase-framework-tools: Experimental addon to the Firebase CLI to add web framework support](https://github.com/FirebaseExtended/firebase-framework-tools)
- (ja) [Next.jsのホスティング先としてFirebaseは『かなりアリ』な選択肢になっている](https://zenn.dev/masakasuno1/articles/0988d547ab1de8)
- (ja) [Firebase CLIのNext.jsデプロイ対応について調べる](https://zenn.dev/laiso/articles/83310ab66881b4)
