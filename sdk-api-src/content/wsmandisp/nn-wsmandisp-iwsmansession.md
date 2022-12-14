---
UID: NN:wsmandisp.IWSManSession
title: IWSManSession (wsmandisp.h)
description: Defines operations and session settings.
helpviewer_keywords: ["IWSManSession","IWSManSession interface [Windows Remote Management]","IWSManSession interface [Windows Remote Management]","described","winrm.iwsmansession","wsmandisp/IWSManSession"]
old-location: winrm\iwsmansession.htm
tech.root: winrm
ms.assetid: 3e016080-339f-4bda-bfd2-f912e090981f
ms.date: 12/05/2018
ms.keywords: IWSManSession, IWSManSession interface [Windows Remote Management], IWSManSession interface [Windows Remote Management],described, winrm.iwsmansession, wsmandisp/IWSManSession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManSession
 - wsmandisp/IWSManSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession
---

# IWSManSession interface


## -description

Defines operations and session settings.  Any Windows Remote Management operations require creation of an <b>IWSManSession</b> object that connects to a remote computer, <a href="/windows/desktop/WinRM/windows-remote-management-glossary">base management controller</a> (BMC), or the local computer. WinRM network operations include getting, writing, enumerating data, or invoking methods.  The methods of the <b>IWSManSession</b> object mirror the basic  operations defined in the WS-Management protocol.

## -inheritance

The <b>IWSManSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManSession</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
