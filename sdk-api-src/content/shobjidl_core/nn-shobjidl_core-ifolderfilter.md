---
UID: NN:shobjidl_core.IFolderFilter
title: IFolderFilter (shobjidl_core.h)
description: Exposed by a client to specify how to filter the enumeration of a Shell folder by a server application.
helpviewer_keywords: ["IFolderFilter","IFolderFilter interface [Windows Shell]","IFolderFilter interface [Windows Shell]","described","_shell_IFolderFilter","shell.IFolderFilter","shobjidl_core/IFolderFilter"]
old-location: shell\IFolderFilter.htm
tech.root: shell
ms.assetid: fd69c11c-f4c3-4681-ae85-385460e96be9
ms.date: 12/05/2018
ms.keywords: IFolderFilter, IFolderFilter interface [Windows Shell], IFolderFilter interface [Windows Shell],described, _shell_IFolderFilter, shell.IFolderFilter, shobjidl_core/IFolderFilter
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IFolderFilter
 - shobjidl_core/IFolderFilter
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
 - IFolderFilter
---

# IFolderFilter interface


## -description

Exposed by a client to specify how to filter the enumeration of a Shell folder by a server application.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFolderFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfilter-getenumflags">GetEnumFlags</a>
</td>
<td align="left" width="63%">
Allows a client to specify which classes of objects in a Shell folder should be enumerated. When used with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a>, specifies the class or classes of items that should be shown in the dialog box tree view and which class or classes should not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfilter-shouldshow">ShouldShow</a>
</td>
<td align="left" width="63%">
Specifies whether an individual item should be allowed through the filter and which should be blocked. When used with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a>, specifies which items should be shown in the dialog box tree view and which should not. The determination to show or not show an item is up to the application.

</td>
</tr>
</table>

## -remarks

This interface is most often used with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a> to filter the contents of the tree view displayed in a folder selection dialog box. To use <b>IFolderFilter</b> with <b>SHBrowseForFolder</b>, the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BIF_NEWDIALOGSTYLE</a> flag must be set.

When your application calls <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a>, you become a client of the folder browser object. The folder browser object communicates with you by sending messages to a callback function, <a href="/previous-versions/windows/desktop/legacy/bb762598(v=vs.85)">BrowseCallbackProc</a>. The <b>BFFM_IUNKNOWN</b> message handled by that callback function contains a pointer to the folder browser's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. To filter the display of a folder's contents, do the following:

                

<ol>
<li>Use the folder browser's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method to request a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite">IFolderFilterSite</a> interface.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfiltersite-setfilter">IFolderFilterSite::SetFilter</a>, passing it a pointer to your <b>IFolderFilter</b> interface.</li>
<li>The folder browser then queries <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfilter-getenumflags">IFolderFilter::GetEnumFlags</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfilter-shouldshow">IFolderFilter::ShouldShow</a>to determine how to filter the enumeration.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite">IFolderFilterSite</a>