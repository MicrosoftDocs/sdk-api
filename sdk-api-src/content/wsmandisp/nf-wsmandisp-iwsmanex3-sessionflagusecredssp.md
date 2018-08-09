---
UID: NF:wsmandisp.IWSManEx3.SessionFlagUseCredSsp
title: IWSManEx3::SessionFlagUseCredSsp
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseCredSsp for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex3_sessionflagusecredssp.htm
old-project: winrm
ms.assetid: 69c62ad1-319e-4716-a2c7-61b931567244
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSManEx3 interface [Windows Remote Management],SessionFlagUseCredSsp method, IWSManEx3.SessionFlagUseCredSsp, IWSManEx3::SessionFlagUseCredSsp, SessionFlagUseCredSsp, SessionFlagUseCredSsp method [Windows Remote Management], SessionFlagUseCredSsp method [Windows Remote Management],IWSManEx3 interface, winrm.iwsmanex3_sessionflagusecredssp, wsmandisp/IWSManEx3::SessionFlagUseCredSsp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx3.SessionFlagUseCredSsp
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx3::SessionFlagUseCredSsp


## -description


Returns the value of the authentication flag <b>WSManFlagUseCredSsp</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUseCredSsp</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out, retval]

Specifies the authentication flag to use.


## -returns



If the method succeeds, it returns the authentication flag. Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/6d362cdf-0f77-446a-8df9-1d38eca853a2">IWSManEx3</a>
 

 

