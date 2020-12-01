---
UID: NF:certadm.ICertAdmin2.GetCAPropertyFlags
title: ICertAdmin2::GetCAPropertyFlags (certadm.h)
description: The ICertAdmin2::GetCAPropertyFlags method retrieves the property flags for a certification authority (CA) property.
helpviewer_keywords: ["CCertAdmin2 object [Security]","GetCAPropertyFlags method","GetCAPropertyFlags","GetCAPropertyFlags method [Security]","GetCAPropertyFlags method [Security]","CCertAdmin2 object","GetCAPropertyFlags method [Security]","ICertAdmin2 interface","ICertAdmin2 interface [Security]","GetCAPropertyFlags method","ICertAdmin2.GetCAPropertyFlags","ICertAdmin2::GetCAPropertyFlags","_certsrv_icertadmin2_getcapropertyflags","certadm/ICertAdmin2::GetCAPropertyFlags","security.icertadmin2_getcapropertyflags"]
old-location: security\icertadmin2_getcapropertyflags.htm
tech.root: security
ms.assetid: 6f38bea1-e278-4085-b321-05f6765cc676
ms.date: 12/05/2018
ms.keywords: CCertAdmin2 object [Security],GetCAPropertyFlags method, GetCAPropertyFlags, GetCAPropertyFlags method [Security], GetCAPropertyFlags method [Security],CCertAdmin2 object, GetCAPropertyFlags method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetCAPropertyFlags method, ICertAdmin2.GetCAPropertyFlags, ICertAdmin2::GetCAPropertyFlags, _certsrv_icertadmin2_getcapropertyflags, certadm/ICertAdmin2::GetCAPropertyFlags, security.icertadmin2_getcapropertyflags
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin2::GetCAPropertyFlags
 - certadm/ICertAdmin2::GetCAPropertyFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetCAPropertyFlags
 - CCertAdmin2.GetCAPropertyFlags
---

# ICertAdmin2::GetCAPropertyFlags


## -description

The <b>GetCAPropertyFlags</b> method retrieves the property flags for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) property. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

The property flags can be examined to determine the data type and to determine whether the property is indexed.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see <b>ICertConfig</b>.

<div class="alert"><b>Important</b>  <b>GetCAPropertyFlags</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.

### -param pPropFlags [out]

A pointer to a value that represents the property flags.

## -returns

<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
A <b>Long</b> representing the property flags.

## -remarks

The <b>LONG</b> value retrieved by calling this method can be examined to determine the data type and the indexed status. To determine the data type and indexed status, use the PROPTYPE_MASK and PROPFLAGS_INDEXED values, respectively.


#### Examples

The following example assumes the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a> interface pointer is valid.


```cpp
BSTR bstrCA = NULL;
LONG nFlags;  // Variable to contain the property flags.

bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
if (NULL == bstrCA)
{
    printf("Failed to allocate memory for bstrCA\n");
    exit(1);
}

// Retrieve a property's flags.
hr = pCertAdmin2->GetCAPropertyFlags(bstrCA,
                                     CR_PROP_EXITCOUNT,
                                     &nFlags);
if (FAILED(hr))
{
    printf("Failed GetCAPropertyFlags\n");
    SysFreeString(bstrCA);
    exit(1);  // Or other error action.
}
// Display the property data type.
switch (nFlags & PROPTYPE_MASK)
{
    case PROPTYPE_BINARY:
        printf("Type is BINARY\n");
        break;
    case PROPTYPE_DATE:
        printf("Type is DATE\n");
        break;
    case PROPTYPE_LONG:
        printf("Type is LONG\n");
        break;
    case PROPTYPE_STRING:
        printf("Type is STRING\n");
        break;
    default:
        printf("Unexpected data type.\n");
        break;
}
// Display the property's indexed status.
printf("Property %s indexed\n", 
       nFlags & PROPFLAGS_INDEXED ? "is" : "is not");

SysFreeString(bstrCA);
```