---
UID: NF:iads.IADsPathname.Retrieve
title: IADsPathname::Retrieve (iads.h)
description: The IADsPathname::Retrieve method retrieves the path of the object with different format types.
helpviewer_keywords: ["IADsPathname interface [ADSI]","Retrieve method","IADsPathname.Retrieve","IADsPathname::Retrieve","Retrieve","Retrieve method [ADSI]","Retrieve method [ADSI]","IADsPathname interface","_ds_iadspathname_retrieve","adsi.iadspathname__retrieve","adsi.iadspathname_retrieve","iads/IADsPathname::Retrieve"]
old-location: adsi\iadspathname_retrieve.htm
tech.root: adsi
ms.assetid: c34f2a5e-5faf-45bf-acc6-8db5fc8bf5fa
ms.date: 12/05/2018
ms.keywords: IADsPathname interface [ADSI],Retrieve method, IADsPathname.Retrieve, IADsPathname::Retrieve, Retrieve, Retrieve method [ADSI], Retrieve method [ADSI],IADsPathname interface, _ds_iadspathname_retrieve, adsi.iadspathname__retrieve, adsi.iadspathname_retrieve, iads/IADsPathname::Retrieve
req.header: iads.h
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsPathname::Retrieve
 - iads/IADsPathname::Retrieve
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPathname.Retrieve
---

# IADsPathname::Retrieve


## -description

The <b>IADsPathname::Retrieve</b> method retrieves the path of the object with different format types.

## -parameters

### -param lnFormatType [in]

Specifies the format that the path should be retrieved in. This can be one of the values specified in the <a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a> enumeration.

### -param pbstrADsPath [out]

Contains a pointer to a <b>BSTR</b> value the receives the object path. The caller must free this memory with the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function when it is no longer required.

## -returns

This method supports the standard return values, as well as the following.

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>