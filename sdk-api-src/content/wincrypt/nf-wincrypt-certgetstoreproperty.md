---
UID: NF:wincrypt.CertGetStoreProperty
title: CertGetStoreProperty function
author: windows-sdk-content
description: Retrieves a store property.
old-location: security\certgetstoreproperty.htm
old-project: seccrypto
ms.assetid: 0df4f18b-3b0f-498e-90a5-74d686af83e0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CertGetStoreProperty, CertGetStoreProperty function [Security], _crypto2_certgetstoreproperty, security.certgetstoreproperty, wincrypt/CertGetStoreProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
 - CertGetStoreProperty
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertGetStoreProperty function


## -description


The <b>CertGetStoreProperty</b> function retrieves a store property.


## -parameters




### -param hCertStore [in]

A handle of an open <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param dwPropId [in]

Indicates one of a range of store properties. There is one predefined store property, CERT_STORE_LOCALIZED_NAME_PROP_ID, the localized name of the store.

User defined properties must be outside the current range of values for predefined context properties. Currently, user defined <i>dwPropId</i> values begin at 4,096.


### -param pvData [out]

A pointer to a buffer that receives the data as determined by <i>dwPropId</i>. For CERT_STORE_LOCALIZED_NAME_PROP_ID, this is the localized name of the store, and <i>pvData</i> points to a null-terminated Unicode wide-character string. For other <i>dwPropId</i>s, <i>pvData</i> points to an array of bytes.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbData [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pvData</i> buffer. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.

If the store property is found, the function returns nonzero, <i>pvData</i> points to the property, and <i>pcbData</i> points to the length of the string. If the store property is not found, the function returns zero and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns CRYPT_E_NOT_FOUND.




## -remarks



Store property identifiers are properties applicable to an entire store. They are not properties on an individual <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL), or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context. Currently, no store properties are persisted.

To find the localized name of a store, you can also use the <a href="https://msdn.microsoft.com/8f0006a9-0930-4b71-87ce-e72371095e4c">CryptFindLocalizedName</a> function.


#### Examples

The following example  shows querying a store for its local name property. Similar code can be used to retrieve other store properties. For a complete example that uses this function, see <a href="https://msdn.microsoft.com/9fb368c9-a0d7-4c5f-9a38-7ef8f7283354">Example C Program: Setting and Getting Certificate Store Properties</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Wincrypt.h&gt;


//--------------------------------------------------------------------
// Declare and initialize variables.
void *pvData = NULL;
DWORD cbData = 0;

//--------------------------------------------------------------------
// Call CertGetStoreProperty a first time
// to get the length of the store name string to be returned.
// hCertStore is a previously assigned HCERTSTORE variable that
// represents an open certificate store.
if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    NULL,     // NULL on the first call  
              // to establish the length of the string
              // to be returned
    &amp;cbData))
{
     printf("The length of the property is %d. \n",cbData);
}
else
{
     printf("The length of the property was not calculated.\n");
     exit(1);
}

//--------------------------------------------------------------------
// cbData is the length of a string to be allocated. 
// Allocate the space for the string and call the function a 
// second time.
if(pvData = malloc(cbData))
{
     printf("%d bytes of memory allocated.\n",cbData);
}
else
{
     printf("Memory was not allocated.\n");
     exit(1);
}

// Call CertGetStoreProperty a second time
// to copy the local store name into the pvData buffer.
if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    pvData,
    &amp;cbData))
{
     printf("The localized name is %S.\n",pvData);
}
else
{
     printf("CertGetStoreProperty failed.\n");
     exit(1);
}

// Free memory when done.
if (pvData)
    free(pvData);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e043486d-9a6e-46c0-b258-6f8d463bf6fe">CertSetStoreProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Store Functions</a>
 

 

