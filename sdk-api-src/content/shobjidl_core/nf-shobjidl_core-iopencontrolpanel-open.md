---
UID: NF:shobjidl_core.IOpenControlPanel.Open
title: IOpenControlPanel::Open (shobjidl_core.h)
description: Opens the specified Control Panel item, optionally to a specific page.
helpviewer_keywords: ["IOpenControlPanel interface [Windows Shell]","Open method","IOpenControlPanel.Open","IOpenControlPanel::Open","Open","Open method [Windows Shell]","Open method [Windows Shell]","IOpenControlPanel interface","_shell_IOpenControlPanel_Open","shell.IOpenControlPanel_Open","shobjidl_core/IOpenControlPanel::Open"]
old-location: shell\IOpenControlPanel_Open.htm
tech.root: shell
ms.assetid: 9485540b-0c3a-46f7-8c79-55991f943809
ms.date: 12/05/2018
ms.keywords: IOpenControlPanel interface [Windows Shell],Open method, IOpenControlPanel.Open, IOpenControlPanel::Open, Open, Open method [Windows Shell], Open method [Windows Shell],IOpenControlPanel interface, _shell_IOpenControlPanel_Open, shell.IOpenControlPanel_Open, shobjidl_core/IOpenControlPanel::Open
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpenControlPanel::Open
 - shobjidl_core/IOpenControlPanel::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenControlPanel.Open
---

# IOpenControlPanel::Open


## -description

Opens the specified Control Panel item, optionally to a specific page.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the item's canonical name as a Unicode string. This parameter is optional and can be <b>NULL</b>. If the calling application passes <b>NULL</b>, then the Control Panel itself opens. For a complete list of Control Panel item canonical names, see <a href="/windows/desktop/shell/controlpanel-canonical-names">Canonical Names of Control Panel Items</a>.

### -param pszPage [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the page within the item to display. This string is appended to the end of the path for Shell folder Control Panel items or appended as a command-line parameter for Control Panel (.cpl) file items. This parameter can be <b>NULL</b>, in which case the first page is shown.

### -param punkSite [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the site for navigating in-frame for Shell folder Control Panel items. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/bb757044(v=msdn.10)">Developing for the Control Panel</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel">IOpenControlPanel</a>