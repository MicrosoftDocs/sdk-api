---
UID: NF:shappmgr.IPublishedApp.Install
title: IPublishedApp::Install (shappmgr.h)
description: Installs an application published by an application publisher. This method is invoked when the user selects Add or Add Later in Add/Remove Programs in Control Panel.
helpviewer_keywords: ["IPublishedApp interface [Windows Shell]","Install method","IPublishedApp.Install","IPublishedApp::Install","Install","Install method [Windows Shell]","Install method [Windows Shell]","IPublishedApp interface","inet_IPublishedApp_Install","shappmgr/IPublishedApp::Install","shell.IPublishedApp_Install"]
old-location: shell\IPublishedApp_Install.htm
tech.root: shell
ms.assetid: 6d8c5720-b48f-4268-810c-c04b14d20d73
ms.date: 12/05/2018
ms.keywords: IPublishedApp interface [Windows Shell],Install method, IPublishedApp.Install, IPublishedApp::Install, Install, Install method [Windows Shell], Install method [Windows Shell],IPublishedApp interface, inet_IPublishedApp_Install, shappmgr/IPublishedApp::Install, shell.IPublishedApp_Install
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPublishedApp::Install
 - shappmgr/IPublishedApp::Install
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp.Install
---

# IPublishedApp::Install


## -description

Installs an application published by an application publisher. This method is invoked when the user selects <b>Add</b> or <b>Add Later</b> in <b>Add/Remove Programs</b> in Control Panel.

## -parameters

### -param pstInstall [in]

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the time the user elected to schedule installation through the <b>Add Later</b> button in <b>Add/Remove Programs</b>. This option is only available if the application supports scheduled installation (compare <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getpossibleactions">GetPossibleActions</a>). If this parameter is <b>NULL</b>, the application should be installed immediately.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getpossibleactions">GetPossibleActions</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>