---
UID: NF:wsmandisp.IWSManEx.SessionFlagNoEncryption
title: IWSManEx::SessionFlagNoEncryption
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagNoEncryption for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagnoencryption.htm
tech.root: winrm
ms.assetid: ec96e873-ecb6-4d89-ada3-41c889544091
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagNoEncryption method, IWSManEx.SessionFlagNoEncryption, IWSManEx::SessionFlagNoEncryption, SessionFlagNoEncryption, SessionFlagNoEncryption method [Windows Remote Management], SessionFlagNoEncryption method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagnoencryption, wsmandisp/IWSManEx::SessionFlagNoEncryption
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx.SessionFlagNoEncryption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManEx::SessionFlagNoEncryption


## -description


The <a href="https://msdn.microsoft.com/15c76f0e-85ae-4ee3-bf9f-ba32195d9adc">WSMan.SessionFlagNoEncryption</a> method returns the value of the authentication flag <b>WSManFlagNoEncryption</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagNoEncryption</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/a921b7bc-1f40-427c-971f-c0bc9c9f6887">Other Session Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/15c76f0e-85ae-4ee3-bf9f-ba32195d9adc">WSMan.SessionFlagNoEncryption</a>
 

 

