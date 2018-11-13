---
UID: NF:certadm.ICertAdmin2.GetCAPropertyFlags
title: ICertAdmin2::GetCAPropertyFlags
author: windows-sdk-content
description: The ICertAdmin2::GetCAPropertyFlags method retrieves the property flags for a certification authority (CA) property.
old-location: security\icertadmin2_getcapropertyflags.htm
tech.root: seccrypto
ms.assetid: 6f38bea1-e278-4085-b321-05f6765cc676
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertAdmin2 object [Security],GetCAPropertyFlags method, GetCAPropertyFlags, GetCAPropertyFlags method [Security], GetCAPropertyFlags method [Security],CCertAdmin2 object, GetCAPropertyFlags method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetCAPropertyFlags method, ICertAdmin2.GetCAPropertyFlags, ICertAdmin2::GetCAPropertyFlags, _certsrv_icertadmin2_getcapropertyflags, certadm/ICertAdmin2::GetCAPropertyFlags, security.icertadmin2_getcapropertyflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin2::GetCAPropertyFlags


## -description


The <b>GetCAPropertyFlags</b> method retrieves the property flags for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) property. This method was first defined in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.

The property flags can be examined to determine the data type and to determine whether the property is indexed.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see <b>ICertConfig</b>.

<div class="alert"><b>Important</b>  <b>GetCAPropertyFlags</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="https://msdn.microsoft.com/8eaa2e36-4358-4abd-a7c2-2c9768766597">ICertAdmin2::GetCAProperty</a>.


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

The following example assumes the <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a> interface pointer is valid.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR bstrCA = NULL;
LONG nFlags;  // Variable to contain the property flags.

bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
if (NULL == bstrCA)
{
    printf("Failed to allocate memory for bstrCA\n");
    exit(1);
}

// Retrieve a property's flags.
hr = pCertAdmin2-&gt;GetCAPropertyFlags(bstrCA,
                                     CR_PROP_EXITCOUNT,
                                     &amp;nFlags);
if (FAILED(hr))
{
    printf("Failed GetCAPropertyFlags\n");
    SysFreeString(bstrCA);
    exit(1);  // Or other error action.
}
// Display the property data type.
switch (nFlags &amp; PROPTYPE_MASK)
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
       nFlags &amp; PROPFLAGS_INDEXED ? "is" : "is not");

SysFreeString(bstrCA);</pre>
</td>
</tr>
</table></span></div>


