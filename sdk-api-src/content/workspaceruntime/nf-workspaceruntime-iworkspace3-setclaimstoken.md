---
UID: NF:workspaceruntime.IWorkspace3.SetClaimsToken
title: IWorkspace3::SetClaimsToken method
author: windows-driver-content
description: Sets the claims token.
old-location: termserv\iworkspace3_setclaimstoken.htm
old-project: TermServ
ms.assetid: 221b0e8f-b43a-4942-9e70-152daf5b1ef0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IWorkspace3, IWorkspace3 interface [Remote Desktop Services], SetClaimsToken method, IWorkspace3::SetClaimsToken, SetClaimsToken method [Remote Desktop Services], SetClaimsToken method [Remote Desktop Services], IWorkspace3 interface, SetClaimsToken,IWorkspace3.SetClaimsToken, termserv.iworkspace3_setclaimstoken, workspaceruntime/IWorkspace3::SetClaimsToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	workspaceruntime.h
api_name:
-	IWorkspace3.SetClaimsToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspace3::SetClaimsToken method


## -description


Sets the claims token.


## -parameters




### -param bstrAccessToken [in]

A string containing the access token.


### -param ullAccessTokenExpiration [in]

The time, in milliseconds, until the access token expires.


### -param bstrRefreshToken [in]

A string containing the refresh token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

