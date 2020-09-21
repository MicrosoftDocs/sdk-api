---
UID: NF:strmif.IFilterMapper3.GetICreateDevEnum
title: IFilterMapper3::GetICreateDevEnum (strmif.h)
description: The GetICreateDevEnum method returns a pointer to the ICreateDevEnum interface. You can use the ICreateDevEnum interface to create an enumerator for a category of filters, such as video capture devices or audio capture devices.
helpviewer_keywords: ["GetICreateDevEnum","GetICreateDevEnum method [DirectShow]","GetICreateDevEnum method [DirectShow]","IFilterMapper3 interface","IFilterMapper3 interface [DirectShow]","GetICreateDevEnum method","IFilterMapper3.GetICreateDevEnum","IFilterMapper3::GetICreateDevEnum","IFilterMapper3GetICreateDevEnum","dshow.ifiltermapper3_geticreatedevenum","strmif/IFilterMapper3::GetICreateDevEnum"]
old-location: dshow\ifiltermapper3_geticreatedevenum.htm
tech.root: dshow
ms.assetid: e54a1276-5c86-4127-9005-f2935e1664d0
ms.date: 12/05/2018
ms.keywords: GetICreateDevEnum, GetICreateDevEnum method [DirectShow], GetICreateDevEnum method [DirectShow],IFilterMapper3 interface, IFilterMapper3 interface [DirectShow],GetICreateDevEnum method, IFilterMapper3.GetICreateDevEnum, IFilterMapper3::GetICreateDevEnum, IFilterMapper3GetICreateDevEnum, dshow.ifiltermapper3_geticreatedevenum, strmif/IFilterMapper3::GetICreateDevEnum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper3::GetICreateDevEnum
 - strmif/IFilterMapper3::GetICreateDevEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper3.GetICreateDevEnum
---

# IFilterMapper3::GetICreateDevEnum


## -description

The <code>GetICreateDevEnum</code> method returns a pointer to the <b>ICreateDevEnum</b> interface. You can use the <a href="/windows/desktop/api/strmif/nn-strmif-icreatedevenum">ICreateDevEnum</a> interface to create an enumerator for a category of filters, such as video capture devices or audio capture devices.


<div class="alert"><b>Note</b>  This method is deprecated. Instead, applications should call <b>CoCreateInstance</b> with CLSID_SystemDeviceEnum to create the <a href="/windows/desktop/DirectShow/system-device-enumerator">System Device Enumerator</a>.</div><div> </div>

## -parameters

### -param ppEnum [out]

Receives a pointer to the <b>ICreateDevEnum</b> interface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper3">IFilterMapper3 Interface</a>