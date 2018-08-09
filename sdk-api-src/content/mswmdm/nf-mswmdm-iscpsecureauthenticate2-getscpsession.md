---
UID: NF:mswmdm.ISCPSecureAuthenticate2.GetSCPSession
title: ISCPSecureAuthenticate2::GetSCPSession
author: windows-sdk-content
description: The GetSCPSession method is used to obtain a pointer to the ISCPSecureQuery interface that represents a session object.
old-location: wmdm\iscpsecureauthenticate2_getscpsession.htm
old-project: WMDM
ms.assetid: 7e09d8ea-65aa-427b-a876-00b089659b1b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSCPSession, GetSCPSession method [windows Media Device Manager], GetSCPSession method [windows Media Device Manager],ISCPSecureAuthenticate2 interface, ISCPSecureAuthenticate2 interface [windows Media Device Manager],GetSCPSession method, ISCPSecureAuthenticate2.GetSCPSession, ISCPSecureAuthenticate2::GetSCPSession, ISCPSecureAuthenticate2GetSCPSession, mswmdm/ISCPSecureAuthenticate2::GetSCPSession, wmdm.iscpsecureauthenticate2_getscpsession
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureAuthenticate2.GetSCPSession
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSecureAuthenticate2::GetSCPSession


## -description



The <b>GetSCPSession</b> method is used to obtain a pointer to the <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a> interface that represents a session object.




## -parameters




### -param ppSCPSession [out]

Pointer to an <a href="https://msdn.microsoft.com/4efd8e5a-490b-435b-b34d-7099198891b1">ISCPSession</a> object.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is used to obtain a secure content provider (SCP) session. An SCP session is useful during transfer of multiple files, where the session can help SCP do some of the operations only once instead of once for every file transfer. This results in better transfer performance.




## -see-also




<a href="https://msdn.microsoft.com/8123f4d2-dcd4-4ff8-a7cf-be8d5f2bf285">ISCPSecureAuthenticate2 Interface</a>
 

 

