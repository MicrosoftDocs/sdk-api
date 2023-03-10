---
UID: NF:mswmdm.IMDSPDevice3.SetProperty
title: IMDSPDevice3::SetProperty (mswmdm.h)
description: The SetProperty method sets a specific device property that is writable.
helpviewer_keywords: ["IMDSPDevice3 interface [windows Media Device Manager]","SetProperty method","IMDSPDevice3.SetProperty","IMDSPDevice3::SetProperty","IMDSPDevice3TransferSessionEnd","SetProperty","SetProperty method [windows Media Device Manager]","SetProperty method [windows Media Device Manager]","IMDSPDevice3 interface","mswmdm/IMDSPDevice3::SetProperty","wmdm.imdspdevice3_setproperty"]
old-location: wmdm\imdspdevice3_setproperty.htm
tech.root: WMDM
ms.assetid: 72bbf8c3-a7e1-4289-b5b0-a57f50d6f46e
ms.date: 12/05/2018
ms.keywords: IMDSPDevice3 interface [windows Media Device Manager],SetProperty method, IMDSPDevice3.SetProperty, IMDSPDevice3::SetProperty, IMDSPDevice3TransferSessionEnd, SetProperty, SetProperty method [windows Media Device Manager], SetProperty method [windows Media Device Manager],IMDSPDevice3 interface, mswmdm/IMDSPDevice3::SetProperty, wmdm.imdspdevice3_setproperty
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
 - IMDSPDevice3::SetProperty
 - mswmdm/IMDSPDevice3::SetProperty
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
 - IMDSPDevice3.SetProperty
---

# IMDSPDevice3::SetProperty


## -description

The <b>SetProperty</b> method sets a specific device property that is writable.

## -parameters

### -param pwszPropName [in]

Name of device property being set.

### -param pValue [in]

Value of device property being set.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method sets the specified device property.

For a list of device property names, see <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

This method is similar to the <b>SetMetadata</b> method for storages, but this method can set only one property at a time.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty">IMDSPDevice3::GetProperty</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-setmetadata">IMDSPStorage3::SetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-getspecifiedmetadata">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>