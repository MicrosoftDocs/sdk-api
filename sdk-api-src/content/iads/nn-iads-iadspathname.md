---
UID: NN:iads.IADsPathname
title: IADsPathname (iads.h)
description: Parses the X.500 and Windows path in ADSI.
helpviewer_keywords: ["IADsPathname","IADsPathname interface [ADSI]","IADsPathname interface [ADSI]","described","Pathname","_ds_iadspathname","adsi.iadspathname","iads/IADsPathname"]
old-location: adsi\iadspathname.htm
tech.root: adsi
ms.assetid: 9aa26d6c-aa86-4a23-a986-b8cb9057772a
ms.date: 12/05/2018
ms.keywords: IADsPathname, IADsPathname interface [ADSI], IADsPathname interface [ADSI],described, Pathname, _ds_iadspathname, adsi.iadspathname, iads/IADsPathname
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
 - IADsPathname
 - iads/IADsPathname
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
 - IADsPathname
 - Pathname
---

# IADsPathname interface


## -description

The <b>IADsPathname</b> interface parses the X.500 and Windows path in ADSI.

The <b>IADsPathname</b> interface can be used to:
<ul>
<li>Set and get paths of ADSI objects in different formats.</li>
<li>Extract or add each element for a given ADsPath.</li>
<li>Construct ADsPaths to be used in queries of directory objects.</li>
</ul>The <b>IADsPathname</b> interface is implemented on a <b>Pathname</b> object. You must instantiate the <b>Pathname</b> object to use the methods defined in the <b>IADsPathname</b> interface. This requirement is similar to calling the  <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance()</a> function in C++.

```cpp
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
```

You can also invoke the <b>New</b> operator in Visual Basic:

```vb
Dim path As New Pathname
```

Or use the <b>CreateObject</b> function in VBScript, supplying "Pathname" as the ProgID.

```vb
Dim path
Set path = CreateObject("Pathname")
```

The <b>IADsPathname</b> interface uses two enumeration types:  <a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a>, and  <a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>.

## -inheritance

The <b>IADsPathname</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPathname</b> also has these types of members:

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance()</a>



<a href="/windows/desktop/ADSI/iadspathname-property-methods">IADsPathname Property
    Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
