---
UID: NF:mswmdm.IMDSPObject.Delete
title: IMDSPObject::Delete (mswmdm.h)
description: The Delete method removes an object or objects from a storage medium on a media device.
helpviewer_keywords: ["Delete","Delete method [windows Media Device Manager]","Delete method [windows Media Device Manager]","IMDSPObject interface","IMDSPObject interface [windows Media Device Manager]","Delete method","IMDSPObject.Delete","IMDSPObject::Delete","IMDSPObjectDelete","mswmdm/IMDSPObject::Delete","wmdm.imdspobject_delete"]
old-location: wmdm\imdspobject_delete.htm
tech.root: WMDM
ms.assetid: debaaa15-dbc5-44dd-8ad9-f7f900146231
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [windows Media Device Manager], Delete method [windows Media Device Manager],IMDSPObject interface, IMDSPObject interface [windows Media Device Manager],Delete method, IMDSPObject.Delete, IMDSPObject::Delete, IMDSPObjectDelete, mswmdm/IMDSPObject::Delete, wmdm.imdspobject_delete
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
 - IMDSPObject::Delete
 - mswmdm/IMDSPObject::Delete
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
 - IMDSPObject.Delete
---

# IMDSPObject::Delete


## -description

The <b>Delete</b> method removes an object or objects from a storage medium on a media device.

## -parameters

### -param fuMode [in]

Flag that must always be set to WMDM_MODE_RECURSIVE by the client. If the object is a folder, it and its contents, and all subfolders and their contents are deleted. If the object is a file, this parameter is ignored.

### -param pProgress [in]

Pointer to an application-implemented <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface that enables the application to receive progress notifications for lengthy <b>Delete</b> operations.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method permanently removes the object(s) from the storage medium.

When using a CompactFlash card reader/writer with Windows Media Device Manager service provider, calling <b>IMDSPObject::Delete</b> immediately after <b>IMDSPObject::Write</b> sometimes fails. This happens because data written to a CompactFlash reader/writer is buffered by the driver of the card reader/writer. The service provider responds as if the write operations are finished, but the driver writes them out to the device according to its own schedule. <b>IMDSPObject::Delete</b> fails if the driver has not finished its writing operation.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>