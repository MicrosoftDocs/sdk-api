---
UID: NN:shobjidl.ISearchBoxInfo
title: ISearchBoxInfo (shobjidl.h)
description: Exposes methods that allow the caller to retrieve information entered into a search box.
helpviewer_keywords: ["ISearchBoxInfo","ISearchBoxInfo interface [Windows Shell]","ISearchBoxInfo interface [Windows Shell]","described","_shell_ISearchBoxInfo","shell.ISearchBoxInfo","shobjidl/ISearchBoxInfo"]
old-location: shell\ISearchBoxInfo.htm
tech.root: shell
ms.assetid: 7b2082e9-b075-488a-a6c1-f9dc99409474
ms.date: 12/05/2018
ms.keywords: ISearchBoxInfo, ISearchBoxInfo interface [Windows Shell], ISearchBoxInfo interface [Windows Shell],described, _shell_ISearchBoxInfo, shell.ISearchBoxInfo, shobjidl/ISearchBoxInfo
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Explorerframe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchBoxInfo
 - shobjidl/ISearchBoxInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ISearchBoxInfo
---

# ISearchBoxInfo interface


## -description

Exposes methods that allow the caller to retrieve information entered into a search box.

## -inheritance

The <b>ISearchBoxInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchBoxInfo</b> also has these types of members:

## -remarks

The search box is shown here in a Windows Explorer window frame.



<img alt="Screen shot of upper-right corner of explorer frame showing search box" src="./images/searchbox.jpg"/>
The frame that contains the search box might also be hosted in another window or in the common file dialog box.

To access the search dialog, use <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> using SID_SSearchBoxInfo on a site pointer within the Windows Explorer window.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows. Third parties do not need to implement their own version.
