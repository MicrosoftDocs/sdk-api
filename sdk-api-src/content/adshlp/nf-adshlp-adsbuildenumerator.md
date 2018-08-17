---
UID: NF:adshlp.ADsBuildEnumerator
title: ADsBuildEnumerator function
author: windows-sdk-content
description: The ADsBuildEnumerator function creates an enumerator object for the specified ADSI container object.
old-location: adsi\adsbuildenumerator.htm
old-project: ADSI
ms.assetid: e4fdec19-bccf-49ec-8a95-29e096c4c9c1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADsBuildEnumerator, ADsBuildEnumerator function [ADSI], _ds_adsbuildenumerator, adshlp/ADsBuildEnumerator, adsi.adsbuildenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsBuildEnumerator
product: Windows
targetos: Windows
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
---

# ADsBuildEnumerator function


## -description


The <b>ADsBuildEnumerator</b> function creates an enumerator object for the specified ADSI container object.


## -parameters




### -param pADsContainer [in]

Type: <b>IADsContainer*</b>

Pointer to the  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface for the object to enumerate.


### -param ppEnumVariant [out]

Type: <b>IEnumVARIANT**</b>

Pointer to an <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface pointer that receives the enumerator object created for the specified container object.


## -returns



Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b> for a successful operation. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <b>ADsBuildEnumerator</b> helper function wraps the calls used to retrieve the <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface on the enumerator object.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b> To enumerate the available objects in a container</b>

<ol>
<li>Call the <b>ADsBuildEnumerator</b> function to create an <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> object that will enumerate the contents of the container.</li>
<li>Call the <a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a> function as many times as necessary to retrieve the items from the enumerator object.</li>
<li>Call the <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> function to release the enumerator object when it is no longer required.</li>
</ol>
If the server supports paged searches and the client has specified a page size that exceeds the maximum search results allowed by the server, the <b>ADsBuildEnumerator</b> function will forward errors and results from the server to the user.


#### Examples

The following code example shows how the <b>ADsBuildEnumerator</b>, <a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>, and <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> functions can be used to enumerate the contents of a container.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT PrintAllObjects(IADsContainer* pContainer)
{
    HRESULT hr;
     
    if(NULL == pContainer) 
    {
        return E_INVALIDARG;
    }
     
    IEnumVARIANT *pEnum = NULL;

    // Create an enumerator object in the container.
    hr = ADsBuildEnumerator(pContainer, &amp;pEnum);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        ULONG ulFetched = 0L;

        // Get the next contained object.
        while(S_OK == (hr = ADsEnumerateNext(pEnum, 1, &amp;var, &amp;ulFetched)) &amp;&amp; (ulFetched &gt; 0))
        {
            IADs *pADs;

            // Print the object
            hr = V_DISPATCH(&amp;var)-&gt;QueryInterface(IID_IADs, (void**)&amp;pADs);
            if(SUCCEEDED(hr))
            {
                CComBSTR sbstr;
                IADsContainer *pChildContainer;

                hr = pADs-&gt;get_Name(&amp;sbstr);
                if(SUCCEEDED(hr))
                {
                    wprintf(sbstr);
                    wprintf(L"\n");
                }

                hr = pADs-&gt;QueryInterface(IID_IADsContainer, (void**)&amp;pChildContainer);
                if(SUCCEEDED(hr))
                {
                    // If the retrieved object is a container, recursively print its contents as well.
                    PrintAllObjects(pChildContainer);
                }
                
                pADs-&gt;Release();
            }
            
            // Release the VARIANT.
            VariantClear(&amp;var);
        }
        
        ADsFreeEnumerator(pEnum);
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>



<a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADsFreeEnumerator</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

