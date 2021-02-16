---
UID: NF:xamlom.IVisualTreeService.AdviseVisualTreeChange
title: IVisualTreeService::AdviseVisualTreeChange (xamlom.h)
description: Starts listening for changes to the visual tree.
helpviewer_keywords: ["AdviseVisualTreeChange","AdviseVisualTreeChange method","AdviseVisualTreeChange method","IVisualTreeService interface","IVisualTreeService interface","AdviseVisualTreeChange method","IVisualTreeService.AdviseVisualTreeChange","IVisualTreeService::AdviseVisualTreeChange","xaml_diagnostics.ivisualtreeservice_advisevisualtreechange","xamlom/IVisualTreeService::AdviseVisualTreeChange"]
old-location: xaml_diagnostics\ivisualtreeservice_advisevisualtreechange.htm
tech.root: xaml_diagnostics
ms.assetid: 83971154-4E40-474C-91AD-2436B1D02CB8
ms.date: 12/05/2018
ms.keywords: AdviseVisualTreeChange, AdviseVisualTreeChange method, AdviseVisualTreeChange method,IVisualTreeService interface, IVisualTreeService interface,AdviseVisualTreeChange method, IVisualTreeService.AdviseVisualTreeChange, IVisualTreeService::AdviseVisualTreeChange, xaml_diagnostics.ivisualtreeservice_advisevisualtreechange, xamlom/IVisualTreeService::AdviseVisualTreeChange
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
 - IVisualTreeService::AdviseVisualTreeChange
 - xamlom/IVisualTreeService::AdviseVisualTreeChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IVisualTreeService.AdviseVisualTreeChange
---

# IVisualTreeService::AdviseVisualTreeChange


## -description

Starts listening for changes to the visual tree.

## -parameters

### -param pCallback [in]

The callback to register for mutation events.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>AdviseVisualTreeChange</b> should be called when the caller wants to start
    listening for mutation events (changes to the visual tree). The callback will start receiving events once 
    the visual tree is constructed. If already constructed, the caller will immediately receive mutation events.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>