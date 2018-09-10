---
UID: NF:wsmandisp.IWSManEx.SessionFlagUseDigest
title: IWSManEx::SessionFlagUseDigest
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseDigest for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagusedigest.htm
tech.root: WinRM
ms.assetid: 3aa44847-932e-49c6-a7fd-966a2bb3539d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUseDigest method, IWSManEx.SessionFlagUseDigest, IWSManEx::SessionFlagUseDigest, SessionFlagUseDigest, SessionFlagUseDigest method [Windows Remote Management], SessionFlagUseDigest method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagusedigest, wsmandisp/IWSManEx::SessionFlagUseDigest
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
 - IWSManEx.SessionFlagUseDigest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManEx::SessionFlagUseDigest


## -description


The <a href="https://msdn.microsoft.com/dba2448a-4f72-4000-8687-4c1be812fc3b">WSMan.SessionFlagUseDigest</a> method returns the value of the authentication flag <b>WSManFlagUseDigest</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUseDigest</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/dba2448a-4f72-4000-8687-4c1be812fc3b">WSMan.SessionFlagUseDigest</a>
 

 

