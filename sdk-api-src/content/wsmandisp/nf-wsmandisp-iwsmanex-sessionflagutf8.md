---
UID: NF:wsmandisp.IWSManEx.SessionFlagUTF8
title: IWSManEx::SessionFlagUTF8
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUTF8 for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagutf8.htm
old-project: winrm
ms.assetid: 99c96057-fbd7-4d8c-a204-1660f84d640f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUTF8 method, IWSManEx.SessionFlagUTF8, IWSManEx::SessionFlagUTF8, SessionFlagUTF8, SessionFlagUTF8 method [Windows Remote Management], SessionFlagUTF8 method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagutf8, wsmandisp/IWSManEx::SessionFlagUTF8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IWSManEx.SessionFlagUTF8
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::SessionFlagUTF8


## -description


The <a href="https://msdn.microsoft.com/a79e292a-364b-4bf3-ae66-6a15ad51524f">WSMan.SessionFlagUTF8</a> method returns the value of the authentication flag <b>WSManFlagUTF8</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUTF8</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/a921b7bc-1f40-427c-971f-c0bc9c9f6887">Other Session Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/a79e292a-364b-4bf3-ae66-6a15ad51524f">WSMan.SessionFlagUTF8</a>
 

 

