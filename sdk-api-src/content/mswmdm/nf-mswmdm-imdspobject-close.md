---
UID: NF:mswmdm.IMDSPObject.Close
title: IMDSPObject::Close (mswmdm.h)
description: The Close method closes a file on a storage medium of a media device.
helpviewer_keywords: ["Close","Close method [windows Media Device Manager]","Close method [windows Media Device Manager]","IMDSPObject interface","IMDSPObject interface [windows Media Device Manager]","Close method","IMDSPObject.Close","IMDSPObject::Close","IMDSPObjectClose","mswmdm/IMDSPObject::Close","wmdm.imdspobject_close"]
old-location: wmdm\imdspobject_close.htm
tech.root: WMDM
ms.assetid: 453dbf9e-4b71-4ceb-80e2-eaa0cf4cd29d
ms.date: 12/05/2018
ms.keywords: Close, Close method [windows Media Device Manager], Close method [windows Media Device Manager],IMDSPObject interface, IMDSPObject interface [windows Media Device Manager],Close method, IMDSPObject.Close, IMDSPObject::Close, IMDSPObjectClose, mswmdm/IMDSPObject::Close, wmdm.imdspobject_close
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
 - IMDSPObject::Close
 - mswmdm/IMDSPObject::Close
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
 - IMDSPObject.Close
---

# IMDSPObject::Close


## -description

The <b>Close</b> method closes a file on a storage medium of a media device.



## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">IMDSPObject::Open</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">IMDSPObject::Read</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a>
