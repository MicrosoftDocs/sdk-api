---
UID: NF:mswmdm.IMDSPDevice2.GetSpecifyPropertyPages
title: IMDSPDevice2::GetSpecifyPropertyPages (mswmdm.h)
description: The GetSpecifyPropertyPages method gets property pages describing non-standard capabilities of portable devices.
helpviewer_keywords: ["GetSpecifyPropertyPages","GetSpecifyPropertyPages method [windows Media Device Manager]","GetSpecifyPropertyPages method [windows Media Device Manager]","IMDSPDevice2 interface","IMDSPDevice2 interface [windows Media Device Manager]","GetSpecifyPropertyPages method","IMDSPDevice2.GetSpecifyPropertyPages","IMDSPDevice2::GetSpecifyPropertyPages","IMDSPDevice2GetSpecifyPropertyPages","mswmdm/IMDSPDevice2::GetSpecifyPropertyPages","wmdm.imdspdevice2_getspecifypropertypages"]
old-location: wmdm\imdspdevice2_getspecifypropertypages.htm
tech.root: WMDM
ms.assetid: e79ce0d2-bfea-4a5b-82f8-9d69f96d9698
ms.date: 12/05/2018
ms.keywords: GetSpecifyPropertyPages, GetSpecifyPropertyPages method [windows Media Device Manager], GetSpecifyPropertyPages method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetSpecifyPropertyPages method, IMDSPDevice2.GetSpecifyPropertyPages, IMDSPDevice2::GetSpecifyPropertyPages, IMDSPDevice2GetSpecifyPropertyPages, mswmdm/IMDSPDevice2::GetSpecifyPropertyPages, wmdm.imdspdevice2_getspecifypropertypages
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
 - IMDSPDevice2::GetSpecifyPropertyPages
 - mswmdm/IMDSPDevice2::GetSpecifyPropertyPages
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
 - IMDSPDevice2.GetSpecifyPropertyPages
---

# IMDSPDevice2::GetSpecifyPropertyPages


## -description

The <b>GetSpecifyPropertyPages</b> method gets property pages describing non-standard capabilities of portable devices.

## -parameters

### -param ppSpecifyPropPages [out]

Pointer to a Win32 <b>ISpecifyPropertyPages</b> interface pointer.

### -param pppUnknowns [out]

Array of <b>IUnknown</b> interface pointers. These interfaces will be passed to the property page and can be used to pass information between the property page and the service provider.

### -param pcUnks [out]

Size of the <i>pppUnknowns</i> array.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Memory for the <i>pppUnknowns</i> array should be allocated by this method and must be freed by the caller using <b>CoTaskMemFree</b>, a standard Win32 function.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>