---
UID: NF:wsmandisp.IWSMan.CreateConnectionOptions
title: IWSMan::CreateConnectionOptions (wsmandisp.h)
author: windows-sdk-content
description: Creates an IWSManConnectionOptions object that specifies the user name and password used when creating a session.
old-location: winrm\iwsman_createconnectionoptions.htm
tech.root: winrm
ms.assetid: e24813cb-b996-4712-803b-360c9bcfdee3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateConnectionOptions, CreateConnectionOptions method [Windows Remote Management], CreateConnectionOptions method [Windows Remote Management],IWSMan interface, IWSMan interface [Windows Remote Management],CreateConnectionOptions method, IWSMan.CreateConnectionOptions, IWSMan::CreateConnectionOptions, winrm.iwsman_createconnectionoptions, wsmandisp/IWSMan::CreateConnectionOptions
ms.topic: method
f1_keywords: ["wsmandisp/IWSMan.CreateConnectionOptions"]
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
 - IWSMan.CreateConnectionOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSMan::CreateConnectionOptions


## -description


Creates an  <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptions">IWSManConnectionOptions</a> object that specifies the user name and password used when  creating a session.


## -parameters




### -param connectionOptions [out]

A pointer to a new <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptions">IWSManConnectionOptions</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsman">IWSMan</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createconnectionoptions">WSMan.CreateConnectionOptions</a>
 

 

