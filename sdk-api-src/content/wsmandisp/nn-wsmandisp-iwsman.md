---
UID: NN:wsmandisp.IWSMan
title: IWSMan (wsmandisp.h)
description: Provides methods and properties used to create a session, represented by a Session object.
helpviewer_keywords: ["IWSMan","IWSMan interface [Windows Remote Management]","IWSMan interface [Windows Remote Management]","described","winrm.iwsman","wsmandisp/IWSMan"]
old-location: winrm\iwsman.htm
tech.root: winrm
ms.assetid: 4e5acfa6-9883-4716-ac69-92161c926c66
ms.date: 12/05/2018
ms.keywords: IWSMan, IWSMan interface [Windows Remote Management], IWSMan interface [Windows Remote Management],described, winrm.iwsman, wsmandisp/IWSMan
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
 - IWSMan
 - wsmandisp/IWSMan
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
 - IWSMan
 - IWSMan.CreateSession
 - IWSMan.CreateConnectionOptions
 - IWSMan.CommandLine
 - IWSMan.get_CommandLine
 - IWSMan.Error
 - IWSMan.get_Error
---

# IWSMan interface


## -description

Provides methods and properties used to create a session, represented by a <a href="/windows/desktop/WinRM/session">Session</a> object. Any Windows Remote Management operations require creation of a <a href="/windows/desktop/WinRM/session">Session</a> that connects to a remote computer, <a href="/windows/desktop/WinRM/windows-remote-management-glossary">base management controller</a> (BMC), or the local computer. Operations include getting, writing, or enumerating data, or invoking methods.

## -inheritance

The <b>IWSMan</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSMan</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WinRM/wsman">WSMan</a>



<a href="/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
