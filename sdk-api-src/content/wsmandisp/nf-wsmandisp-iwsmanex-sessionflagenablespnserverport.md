---
UID: NF:wsmandisp.IWSManEx.SessionFlagEnableSPNServerPort
title: IWSManEx::SessionFlagEnableSPNServerPort
author: windows-driver-content
description: Returns the value of the authentication flag WSManFlagEnableSPNServerPort for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagenablespnserverport.htm
old-project: WinRM
ms.assetid: a8fe2077-0606-4517-8e50-dc42a4c39b77
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagEnableSPNServerPort method, IWSManEx.SessionFlagEnableSPNServerPort, IWSManEx::SessionFlagEnableSPNServerPort, SessionFlagEnableSPNServerPort, SessionFlagEnableSPNServerPort method [Windows Remote Management], SessionFlagEnableSPNServerPort method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagenablespnserverport, wsmandisp/IWSManEx::SessionFlagEnableSPNServerPort
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
-	IWSManEx.SessionFlagEnableSPNServerPort
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::SessionFlagEnableSPNServerPort


## -description


The <a href="https://msdn.microsoft.com/a18a87e6-dcee-4e9f-8e8c-262fef36ab1a">WSMan.SessionFlagEnableSPNServerPort</a> method returns the value of the authentication flag <b>WSManFlagEnableSPNServerPort</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagEnableSPNServerPort</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/a921b7bc-1f40-427c-971f-c0bc9c9f6887">Other Session Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/a18a87e6-dcee-4e9f-8e8c-262fef36ab1a">WSMan.SessionFlagEnableSPNServerPort</a>
 

 

