---
UID: NF:shobjidl_core.IExplorerBrowser.BrowseToIDList
title: IExplorerBrowser::BrowseToIDList (shobjidl_core.h)
description: Browses to a pointer to an item identifier list (PIDL)
helpviewer_keywords: ["BrowseToIDList","BrowseToIDList method [Windows Shell]","BrowseToIDList method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","BrowseToIDList method","IExplorerBrowser.BrowseToIDList","IExplorerBrowser::BrowseToIDList","SBSP_ABSOLUTE","SBSP_KEEPWORDWHEELTEXT","SBSP_NAVIGATEBACK","SBSP_NAVIGATEFORWARD","SBSP_PARENT","SBSP_RELATIVE","_shell_IExplorerBrowser_BrowseToIDList","shell.IExplorerBrowser_BrowseToIDList","shobjidl_core/IExplorerBrowser::BrowseToIDList"]
old-location: shell\IExplorerBrowser_BrowseToIDList.htm
tech.root: shell
ms.assetid: b0633072-e059-4ea4-b9c0-798399ccf66a
ms.date: 12/05/2018
ms.keywords: BrowseToIDList, BrowseToIDList method [Windows Shell], BrowseToIDList method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],BrowseToIDList method, IExplorerBrowser.BrowseToIDList, IExplorerBrowser::BrowseToIDList, SBSP_ABSOLUTE, SBSP_KEEPWORDWHEELTEXT, SBSP_NAVIGATEBACK, SBSP_NAVIGATEFORWARD, SBSP_PARENT, SBSP_RELATIVE, _shell_IExplorerBrowser_BrowseToIDList, shell.IExplorerBrowser_BrowseToIDList, shobjidl_core/IExplorerBrowser::BrowseToIDList
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
 - IExplorerBrowser::BrowseToIDList
 - shobjidl_core/IExplorerBrowser::BrowseToIDList
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
 - IExplorerBrowser.BrowseToIDList
---

# IExplorerBrowser::BrowseToIDList


## -description

Browses to a pointer to an item identifier list (PIDL)

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a const <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (item identifier list) that specifies an object's location as the destination to navigate to. This parameter can be <b>NULL</b>. For more information, see Remarks.

### -param uFlags [in]

Type: <b>UINT</b>

A flag that specifies the category of the <i>pidl</i>. This affects how navigation is accomplished. Must be the value zero, or a bitwise combination of the following values.



#### SBSP_ABSOLUTE

An absolute PIDL, relative to the desktop.



#### SBSP_RELATIVE

A relative PIDL, relative to the current folder.



#### SBSP_PARENT

Browse to the parent folder, ignore the PIDL.



#### SBSP_NAVIGATEBACK

Navigate back, ignore the PIDL.



#### SBSP_NAVIGATEFORWARD

Navigate forward, ignore the PIDL.





#### SBSP_KEEPWORDWHEELTEXT

<b>Windows Vista and later</b>. This flag indicates that any search text entered by a WordWheel (the Search box in Windows Explorer) should be preserved during this navigation, so that items at the new location are filtered in the same way they were filtered at the previous location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The parameter <i>pidl</i> may be <b>NULL</b> if the flags specified in <i>uFlags</i> indicate navigation through the built-in TravelLog, that is, SBSP_NAVIGATEBACK or SBSP_NAVIGATEFORWARD.

 This method supports only a subset of the SBSP flags listed in the shobjidl.h file. Consequently, this method returns E_INVALIDARG if SBSP_NEWBROWSER or SBSP_EXPLOREMODE are specified in <i>uFlags</i>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-browseobject">BrowseObject</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>