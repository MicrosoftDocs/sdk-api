---
UID: NF:winsxs.IAssemblyCacheItem.Commit
title: IAssemblyCacheItem::Commit (winsxs.h)
description: The Commit method copies information into the side-by-side store. When this method returns, the assembly is visible in the side-by-side store.
helpviewer_keywords: ["Commit","Commit method [Side-by-side Assemblies]","Commit method [Side-by-side Assemblies]","IAssemblyCacheItem interface","IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED","IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED","IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED","IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH","IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH","IAssemblyCacheItem interface [Side-by-side Assemblies]","Commit method","IAssemblyCacheItem.Commit","IAssemblyCacheItem::Commit","setup.iassemblycacheitem_commit","winsxs/IAssemblyCacheItem::Commit"]
old-location: setup\iassemblycacheitem_commit.htm
tech.root: setup
ms.assetid: d8f8b6b3-72b4-400b-a780-fc25d1f4b9d0
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Side-by-side Assemblies], Commit method [Side-by-side Assemblies],IAssemblyCacheItem interface, IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED, IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED, IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED, IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH, IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH, IAssemblyCacheItem interface [Side-by-side Assemblies],Commit method, IAssemblyCacheItem.Commit, IAssemblyCacheItem::Commit, setup.iassemblycacheitem_commit, winsxs/IAssemblyCacheItem::Commit
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Sxs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAssemblyCacheItem::Commit
 - winsxs/IAssemblyCacheItem::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyCacheItem.Commit
---

# IAssemblyCacheItem::Commit


## -description

The <b>Commit</b> method copies information into the side-by-side store. When this method returns, the assembly is visible in the side-by-side store.

## -parameters

### -param dwFlags [in]

This parameter specifies how existing information in the side-by-side store is to be replaced by information for the assembly being installed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH"></a><a id="iassemblycacheitem_commit_flag_refresh"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing information in the side-by-side store with the information in the assembly being installed if the version in the assembly is greater than or equal to the version of the existing information. This is the default option.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH"></a><a id="iassemblycacheitem_commit_flag_force_refresh"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing information in the side-by-side store with the information for the assembly being installed.

</td>
</tr>
</table>

### -param pulDisposition [out, optional]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED"></a><a id="iassemblycacheitem_commit_disposition_installed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly is installed for the first time.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED"></a><a id="iassemblycacheitem_commit_disposition_refreshed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED</b></dt>
</dl>
</td>
<td width="60%">
The assembly replaces an existing assembly.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED"></a><a id="iassemblycacheitem_commit_disposition_already_installed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly is already installed in the side-by-side assembly store.

</td>
</tr>
</table>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsxs/nn-winsxs-iassemblycacheitem">IAssemblyCacheItem</a>