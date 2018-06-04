---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICEnroll::enumProviders


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumProviders</b> method retrieves the names of the available <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) specified by the 
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property. This method was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the CSP whose name will be retrieved. Specify zero for the first CSP.


### -param dwFlags [in]

Specifies flags that are passed through to the <a href="https://msdn.microsoft.com/2d93ef0f-b48f-481b-ba62-c535476fde08">CryptEnumProviders</a> function. This parameter is not currently used; specify zero.


### -param pbstrProvName [out]

A pointer to a <b>BSTR</b> variable that receives the name of a CSP with the specified property type. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more CSPs with the property type indicated by the 
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.

<h3>VB</h3>
 The return value is a <b>String</b> variable that contains the name of a CSP. An exception is raised if an error is encountered or when there are no more items.




## -remarks



If the 
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property value has not been set, the default value (usually PROV_RSA_FULL) of <b>ProviderType</b> as set in the registry, is used.

The <b>enumProviders</b> method  calls the 
<a href="https://msdn.microsoft.com/2d93ef0f-b48f-481b-ba62-c535476fde08">CryptEnumProviders</a> function.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR       bstrProvName = NULL;
DWORD      nProv;
int        j;
HRESULT    hr;

// array of CSP provider types (see Wincrypt.h)
DWORD      nProvType[] = { PROV_RSA_FULL,      
                           PROV_RSA_SIG,       
                           // list shortened for brevity
                           //...
                           PROV_STT_ISS };

// Loop, for each Prov Type.
for (j = 0; j &lt; (sizeof(nProvType)/sizeof(DWORD)); j++)
{
    nProv = 0;
    
    // pEnroll is previously instantiated ICEnroll interface pointer
    hr = pEnroll-&gt;put_ProviderType( nProvType[j] );
    if ( FAILED(hr))
    {
        printf("Failed put_ProviderType - %x\n", hr);
        goto error;
    }
    // Enumerate the CSPs of this type.
    while ( S_OK == ( hr = pEnroll-&gt;enumProviders(nProv,
                                                  0,
                                                  &amp;bstrProvName)))
    {
        printf("Provider %ws (type %d )\n", bstrProvName, 
            nProvType[j] );
        nProv++;
        if ( bstrProvName )
        {
            SysFreeString( bstrProvName );
            bstrProvName = NULL;
        }
    }

    // Print message if provider type does not have any CSPs.
    if ( 0 == nProv )
       printf("There were no CSPs of type %d\n", dwType );
}

error:
// Clean up resources, and so on.
if ( bstrProvName )
    SysFreeString( bstrProvName );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a>
 

 

