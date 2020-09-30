---
UID: NS:adsprop._ADSPROPINITPARAMS
title: ADSPROPINITPARAMS (adsprop.h)
description: Used with the ADsPropGetInitInfo function to obtain object data that a display specifier applies to.
helpviewer_keywords: ["*PADSPROPINITPARAMS","ADSPROPINITPARAMS","ADSPROPINITPARAMS structure [Active Directory]","PADSPROPINITPARAMS","PADSPROPINITPARAMS structure pointer [Active Directory]","_glines_adspropinitparams","ad.adspropinitparams","adsprop/ADSPROPINITPARAMS","adsprop/PADSPROPINITPARAMS"]
old-location: ad\adspropinitparams.htm
tech.root: ad
ms.assetid: cbee3515-5037-4d65-8817-4c63fe13ef5d
ms.date: 12/05/2018
ms.keywords: '*PADSPROPINITPARAMS, ADSPROPINITPARAMS, ADSPROPINITPARAMS structure [Active Directory], PADSPROPINITPARAMS, PADSPROPINITPARAMS structure pointer [Active Directory], _glines_adspropinitparams, ad.adspropinitparams, adsprop/ADSPROPINITPARAMS, adsprop/PADSPROPINITPARAMS'
req.header: adsprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADSPROPINITPARAMS, *PADSPROPINITPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADSPROPINITPARAMS
 - adsprop/_ADSPROPINITPARAMS
 - PADSPROPINITPARAMS
 - adsprop/PADSPROPINITPARAMS
 - ADSPROPINITPARAMS
 - adsprop/ADSPROPINITPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Adsprop.h
api_name:
 - ADSPROPINITPARAMS
---

# ADSPROPINITPARAMS structure


## -description

The <b>ADSPROPINITPARAMS</b> structure is used with the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropgetinitinfo">ADsPropGetInitInfo</a> function to obtain object data that a display specifier applies to.

## -struct-fields

### -field dwSize

The size, in bytes, of the <b>ADSPROPINITPARAMS</b> structure. Set this value before calling <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropgetinitinfo">ADsPropGetInitInfo</a>.

### -field dwFlags

Reserved.

### -field hr

Contains an <b>HRESULT</b> value that specifies the result of the bind/get operation. If this value does not equal <b>S_OK</b>, then the remaining structure members are not initialized and should be ignored.

### -field pDsObj

Pointer to an <a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a> interface that represents the directory object that the display specifier applies to. Do not release this interface.

### -field pwzCN

Pointer to a null-terminated Unicode string that contains the common name of the directory object.

### -field pWritableAttrs

Pointer to an <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a> structure that contains attribute data for the directory object.

## -remarks

The <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropgetinitinfo">ADsPropGetInitInfo</a> function allocates memory  for the <b>pwzCN</b> and <b>pWritableAttrs</b> members. This memory is freed by the system after all display specifier objects are destroyed. The reference count for the interface pointer in <b>pDsObj</b> is not incremented by calling <b>ADsPropGetInitInfo</b>, so the interface must not be released by the caller.

## -see-also

<a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropgetinitinfo">ADsPropGetInitInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>