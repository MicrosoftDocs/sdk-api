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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPathname</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPathname</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPathname</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-addleafelement">AddLeafElement</a>
</td>
<td align="left" width="63%">
Adds an element to the end of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-copypath">CopyPath</a>
</td>
<td align="left" width="63%">
Generates an object with the same path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-getelement">GetElement</a>
</td>
<td align="left" width="63%">
Gets elements stored in the object with its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-getescapedelement">GetEscapedElement</a>
</td>
<td align="left" width="63%">
Escapes an RDN string and returns the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-getnumelements">GetNumElements</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-removeleafelement">RemoveLeafElement</a>
</td>
<td align="left" width="63%">
Removes the last element from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-retrieve">Retrieve</a>
</td>
<td align="left" width="63%">
Retrieves an object path with an <a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-set">Set</a>
</td>
<td align="left" width="63%">
Sets an object path with an <a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a> option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iadspathname-setdisplaytype">SetDisplayType</a>
</td>
<td align="left" width="63%">
Specifies how a path is to be displayed.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPathname</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iadspathname-property-methods">EscapedMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves the mode for escaping a path.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance()</a>



<a href="/windows/desktop/ADSI/iadspathname-property-methods">IADsPathname Property
    Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>