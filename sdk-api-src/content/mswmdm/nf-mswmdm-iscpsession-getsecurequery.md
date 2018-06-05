---
UID: NF:mswmdm.ISCPSession.GetSecureQuery
title: ISCPSession::GetSecureQuery
author: windows-sdk-content
description: The GetSecureQuery method is used to obtain a secure query object for the session.
old-location: wmdm\iscpsession_getsecurequery.htm
old-project: WMDM
ms.assetid: c725f0ae-1f37-412d-ac2b-0833989d1bd6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetSecureQuery, GetSecureQuery method [windows Media Device Manager], GetSecureQuery method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],GetSecureQuery method, ISCPSession.GetSecureQuery, ISCPSession::GetSecureQuery, ISCPSessionGetSecureQuerry, mswmdm/ISCPSession::GetSecureQuery, wmdm.iscpsession_getsecurequery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	ISCPSession.GetSecureQuery
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSession::GetSecureQuery


## -description



The <b>GetSecureQuery</b> method is used to obtain a secure query object for the session.




## -parameters




### -param ppSecureQuery [out]

Pointer to a secure query object.


## -returns



If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method should be used to obtain a secure query object when using secure content provider sessions for efficient transfer of multiple files.




## -see-also




<a href="https://msdn.microsoft.com/4efd8e5a-490b-435b-b34d-7099198891b1">ISCPSession Interface</a>
 

 

