---
UID: NF:wsmandisp.IWSManEx.SessionFlagSkipCACheck
title: IWSManEx::SessionFlagSkipCACheck
author: windows-driver-content
description: Returns the value of the WSManFlagSkipCACheck authentication flag for use in the flags parameter of the IWSMan::CreateSession method.
old-location: winrm\iwsmanex_sessionflagskipcacheck.htm
old-project: WinRM
ms.assetid: 683054fd-7ee3-4c90-a5cd-234e7d60349d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagSkipCACheck method, IWSManEx.SessionFlagSkipCACheck, IWSManEx::SessionFlagSkipCACheck, SessionFlagSkipCACheck, SessionFlagSkipCACheck method [Windows Remote Management], SessionFlagSkipCACheck method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagskipcacheck, wsmandisp/IWSManEx::SessionFlagSkipCACheck
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSManProxyAuthenticationFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WSMAuto.dll
api_name:
-	IWSManEx.SessionFlagSkipCACheck
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::SessionFlagSkipCACheck


## -description


The <a href="https://msdn.microsoft.com/a67cadb3-c20a-4a58-a13b-5bbd23c547d1">WSMan.SessionFlagSkipCACheck</a> method returns the value of the  <b>WSManFlagSkipCACheck</b> authentication flag for use in the <i>flags</i> parameter of the <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a> method.

<b>WSManFlagSkipCACheck</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/a67cadb3-c20a-4a58-a13b-5bbd23c547d1">WSMan.SessionFlagSkipCACheck</a>
 

 

