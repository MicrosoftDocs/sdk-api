---
UID: NF:shobjidl_core.IExplorerBrowser.RemoveAll
title: IExplorerBrowser::RemoveAll (shobjidl_core.h)

description: Removes all items from the results folder.
old-location: shell\IExplorerBrowser_RemoveAll.htm
tech.root: shell
ms.assetid: 4447d3f4-659f-4ec1-8a6f-91031c85b704

ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],RemoveAll method, IExplorerBrowser.RemoveAll, IExplorerBrowser::RemoveAll, RemoveAll, RemoveAll method [Windows Shell], RemoveAll method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_RemoveAll, shell.IExplorerBrowser_RemoveAll, shobjidl_core/IExplorerBrowser::RemoveAll
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IExplorerBrowser.RemoveAll"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.RemoveAll
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerBrowser::RemoveAll


## -description


Removes all items from the results folder.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or  E_UNEXPECTED if this method is called before a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject">IExplorerBrowser::FillFromObject</a>.




## -remarks



This method removes all results from the  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iresultsfolder">IResultsFolder</a> created in method <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject">IExplorerBrowser::FillFromObject</a>.



