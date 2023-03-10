---
UID: NN:wsmandisp.IWSManConnectionOptions
title: IWSManConnectionOptions (wsmandisp.h)
description: The IWSManConnectionOptions object is passed to the IWSMan::CreateSession method to provide the user name and password associated with the local account on the remote computer.
helpviewer_keywords: ["IWSManConnectionOptions","IWSManConnectionOptions interface [Windows Remote Management]","IWSManConnectionOptions interface [Windows Remote Management]","described","winrm.iwsmanconnectionoptions","wsmandisp/IWSManConnectionOptions"]
old-location: winrm\iwsmanconnectionoptions.htm
tech.root: winrm
ms.assetid: 940097da-c5bb-4170-a2aa-fcbbee622fe6
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptions, IWSManConnectionOptions interface [Windows Remote Management], IWSManConnectionOptions interface [Windows Remote Management],described, winrm.iwsmanconnectionoptions, wsmandisp/IWSManConnectionOptions
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
 - IWSManConnectionOptions
 - wsmandisp/IWSManConnectionOptions
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
 - IWSManConnectionOptions
---

# IWSManConnectionOptions interface


## -description

The <b>IWSManConnectionOptions</b> object is passed to the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a> method to provide the user name and password associated with the local account on the remote computer. If no parameters are supplied, then the credentials of the account running the script are the default values.

## -remarks

If a   Windows Remote Management client application  is running under impersonation, then a failure occurs if you set  the <a href="/windows/desktop/WinRM/connectionoptions-password">Password</a> property. A client application is a script or other program that sends a request to  WinRM on the local or a remote computer. The client application may be running under impersonation because it called a function like <a href="/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)">ImpersonateClient</a>. An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.

## -see-also

<a href="/windows/desktop/WinRM/connectionoptions">ConnectionOptions</a>



<a href="/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>