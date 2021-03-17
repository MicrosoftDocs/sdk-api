---
UID: NF:mswmdm.IMDSPObject.Rename
title: IMDSPObject::Rename (mswmdm.h)
description: The Rename method renames the associated object which can be a file or a folder.
helpviewer_keywords: ["IMDSPObject interface [windows Media Device Manager]","Rename method","IMDSPObject.Rename","IMDSPObject::Rename","IMDSPObjectRename","Rename","Rename method [windows Media Device Manager]","Rename method [windows Media Device Manager]","IMDSPObject interface","mswmdm/IMDSPObject::Rename","wmdm.imdspobject_rename"]
old-location: wmdm\imdspobject_rename.htm
tech.root: WMDM
ms.assetid: 3da6a4a4-6e3b-4907-a466-5a5bd34f4374
ms.date: 12/05/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Rename method, IMDSPObject.Rename, IMDSPObject::Rename, IMDSPObjectRename, Rename, Rename method [windows Media Device Manager], Rename method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Rename, wmdm.imdspobject_rename
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPObject::Rename
 - mswmdm/IMDSPObject::Rename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject.Rename
---

# IMDSPObject::Rename


## -description

The <b>Rename</b> method renames the associated object which can be a file or a folder.

## -parameters

### -param pwszNewName [in]

Pointer to a wide-character null-terminated string to receive a new name for the object. For information on how to use the <b>LPWSTR</b> variable type, see the Windows documentation.

### -param pProgress [in]

Pointer to an application-implemented <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface that enables the application to receive progress notification for lengthy renaming operations.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>