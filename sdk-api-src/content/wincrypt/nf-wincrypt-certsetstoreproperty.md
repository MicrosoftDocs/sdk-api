---
UID: NF:wincrypt.CertSetStoreProperty
title: CertSetStoreProperty function
author: windows-sdk-content
description: The CertSetStoreProperty function sets a store property.
old-location: security\certsetstoreproperty.htm
old-project: SecCrypto
ms.assetid: e043486d-9a6e-46c0-b258-6f8d463bf6fe
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CertSetStoreProperty, CertSetStoreProperty function [Security], _crypto2_certsetstoreproperty, security.certsetstoreproperty, wincrypt/CertSetStoreProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertSetStoreProperty
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertSetStoreProperty function


## -description


The <b>CertSetStoreProperty</b> function sets a store property.


## -parameters




### -param hCertStore [in]

Handle for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.
					


### -param dwPropId [in]

Indicates one of a range of store properties. Values for user-defined properties must be outside the current range of predefined context property values. Currently, user-defined <i>dwPropId</i> values begin at 4,096. There is one predefined store property, CERT_STORE_LOCALIZED_NAME_PROP_ID, the localized name of the store.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pvData [in]

The type definition for <i>pvData</i> depends on the <i>dwPropId</i> value. If <i>dwPropId</i> is CERT_STORE_LOCALIZED_NAME_PROP_ID, <i>pvData</i> points to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure. The <b>pbData</b> member of that structure is a pointer to a <b>null</b>-terminated Unicode character string. The <b>cbData</b> member of that structure is a <b>DWORD</b> value holding the length of the string. 




For user-defined <i>dwPropId</i> values, <i>pvData</i> is a pointer to an encoded <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a>.

If a value already exists for the selected property, the old value is replaced.

Calling this function with <i>pvData</i> set to <b>NULL</b> deletes a property.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



Store property identifiers are properties applicable to an entire store. They are not properties for an individual <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a>, or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a> context. Currently, no store properties are persisted.


#### Examples

The following example shows setting the localized name property of an open certificate store.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//--------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE hCertStore = NULL;       // Original certificate store
CRYPT_DATA_BLOB Property_Name_Blob; // BLOB to hold store property

//--------------------------------------------------------------
// Open the certificate store that will have its localized name
// property set. In this case, the CA system store is opened. 

if ( hCertStore = CertOpenStore(
    CERT_STORE_PROV_SYSTEM,
    0,
    NULL,
    CERT_SYSTEM_STORE_CURRENT_USER,
    L"CA"))
{
     printf("The CA store is open.\n");
}
else
{
     printf("The CA store could not be opened \n.");
     exit(1);
}

//--------------------------------------------------------------------
// Prepare a data structure to set a store property.
// Initialize the members of the CRYPT_DATA_BLOB.
Property_Name_Blob.pbData = (BYTE *) L"The Local CA Store";
Property_Name_Blob.cbData = 
       (wcslen((LPWSTR)Property_Name_Blob.pbData)+1) * sizeof(WCHAR);

//--------------------------------------------------------------------
// Set the store's localized name property.
if (CertSetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    0,
    &amp;Property_Name_Blob))
{
     printf("The name of the store has been set. Continue. \n");
}
else
{
     printf("Setting the store's localized name failed.\n");
     exit(1);
}

// Close the store when done.
if (!CertCloseStore(
     hCertStore,
     0 ))
{
     printf("The CA store could not be closed \n.");
     exit(1);

}</pre>
</td>
</tr>
</table></span></div>
For another  example that uses this function, see <a href="https://msdn.microsoft.com/9fb368c9-a0d7-4c5f-9a38-7ef8f7283354">Example C Program: Setting and Getting Certificate Store Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0df4f18b-3b0f-498e-90a5-74d686af83e0">CertGetStoreProperty</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

