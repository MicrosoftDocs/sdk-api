---
UID: NF:mswmdm.IWMDMDevice2.GetSpecifyPropertyPages
title: IWMDMDevice2::GetSpecifyPropertyPages (mswmdm.h)
description: The GetSpecifyPropertyPages method retrieves the property page for the device. Property pages can be used to report device-specific properties and branding information.
helpviewer_keywords: ["GetSpecifyPropertyPages","GetSpecifyPropertyPages method [windows Media Device Manager]","GetSpecifyPropertyPages method [windows Media Device Manager]","IWMDMDevice2 interface","IWMDMDevice2 interface [windows Media Device Manager]","GetSpecifyPropertyPages method","IWMDMDevice2.GetSpecifyPropertyPages","IWMDMDevice2::GetSpecifyPropertyPages","IWMDMDevice2GetSpecifyPropertyPages","mswmdm/IWMDMDevice2::GetSpecifyPropertyPages","wmdm.iwmdmdevice2_getspecifypropertypages"]
old-location: wmdm\iwmdmdevice2_getspecifypropertypages.htm
tech.root: WMDM
ms.assetid: bc46af60-5d74-4ac6-b680-c47b55c444e0
ms.date: 12/05/2018
ms.keywords: GetSpecifyPropertyPages, GetSpecifyPropertyPages method [windows Media Device Manager], GetSpecifyPropertyPages method [windows Media Device Manager],IWMDMDevice2 interface, IWMDMDevice2 interface [windows Media Device Manager],GetSpecifyPropertyPages method, IWMDMDevice2.GetSpecifyPropertyPages, IWMDMDevice2::GetSpecifyPropertyPages, IWMDMDevice2GetSpecifyPropertyPages, mswmdm/IWMDMDevice2::GetSpecifyPropertyPages, wmdm.iwmdmdevice2_getspecifypropertypages
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
 - IWMDMDevice2::GetSpecifyPropertyPages
 - mswmdm/IWMDMDevice2::GetSpecifyPropertyPages
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
 - IWMDMDevice2.GetSpecifyPropertyPages
---

# IWMDMDevice2::GetSpecifyPropertyPages


## -description

The <b>GetSpecifyPropertyPages</b> method retrieves the property page for the device. Property pages can be used to report device-specific properties and branding information.

## -parameters

### -param ppSpecifyPropPages [out]

Pointer to a pointer to an <b>ISpecifyPropertyPages</b> interface. <b>ISpecifyPropertyPages</b> is documented in the COM area of the Platform SDK. The caller must release this interface when done with it.

### -param pppUnknowns [out]

Specifies an array of <b>IUnknown</b> interface pointers. These interfaces are passed to the property page and can be used to pass information between the property page and the service provider. The array is allocated by Windows Media Device Manager, but the caller must call <b>Release</b> on each interface retrieved, and <b>CoTaskMemFree</b> on the retrieved array.

### -param pcUnks [out]

Retrieves the size of the <i>pppUnknowns</i> array.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2 Interface</a>