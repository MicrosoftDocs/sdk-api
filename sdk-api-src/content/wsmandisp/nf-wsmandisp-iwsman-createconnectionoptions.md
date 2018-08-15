---
UID: NF:wsmandisp.IWSMan.CreateConnectionOptions
title: IWSMan::CreateConnectionOptions
author: windows-sdk-content
description: Creates an IWSManConnectionOptions object that specifies the user name and password used when creating a session.
old-location: winrm\iwsman_createconnectionoptions.htm
old-project: winrm
ms.assetid: e24813cb-b996-4712-803b-360c9bcfdee3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateConnectionOptions, CreateConnectionOptions method [Windows Remote Management], CreateConnectionOptions method [Windows Remote Management],IWSMan interface, IWSMan interface [Windows Remote Management],CreateConnectionOptions method, IWSMan.CreateConnectionOptions, IWSMan::CreateConnectionOptions, winrm.iwsman_createconnectionoptions, wsmandisp/IWSMan::CreateConnectionOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.redist: 
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
 - IWSMan.CreateConnectionOptions
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSMan::CreateConnectionOptions


## -description


Creates an  <a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a> object that specifies the user name and password used when  creating a session.


## -parameters




### -param connectionOptions [out]

A pointer to a new <a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4e5acfa6-9883-4716-ac69-92161c926c66">IWSMan</a>



<a href="https://msdn.microsoft.com/3669a5fe-8305-4fa3-aa75-fafefcd8b33d">WSMan.CreateConnectionOptions</a>
 

 

