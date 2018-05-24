---
UID: NF:mswmdm.ISCPSecureAuthenticate.GetSecureQuery
title: ISCPSecureAuthenticate::GetSecureQuery
author: windows-driver-content
description: The GetSecureQuery method is used to obtain a pointer to the ISCPSecureQuery interface.
old-location: wmdm\iscpsecureauthenticate_getsecurequery.htm
old-project: WMDM
ms.assetid: d0cee36c-5200-4951-9a83-a0f32658939b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetSecureQuery, GetSecureQuery method [windows Media Device Manager], GetSecureQuery method [windows Media Device Manager],ISCPSecureAuthenticate interface, ISCPSecureAuthenticate interface [windows Media Device Manager],GetSecureQuery method, ISCPSecureAuthenticate.GetSecureQuery, ISCPSecureAuthenticate::GetSecureQuery, ISCPSecureAuthenticateGetSecureQuery, mswmdm/ISCPSecureAuthenticate::GetSecureQuery, wmdm.iscpsecureauthenticate_getsecurequery
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ISCPSecureAuthenticate.GetSecureQuery
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSecureAuthenticate::GetSecureQuery


## -description



The <b>GetSecureQuery</b> method is used to obtain a pointer to the <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a> interface.




## -parameters




### -param ppSecureQuery [out]

Pointer to an <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a> object.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dfe37b41-f80b-4992-84c1-c23581cc4b69">ISCPSecureAuthenticate Interface</a>



<a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery Interface</a>
 

 

