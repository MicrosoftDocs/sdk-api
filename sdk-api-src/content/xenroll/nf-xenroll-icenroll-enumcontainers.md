---
UID: NF:xenroll.ICEnroll.enumContainers
title: ICEnroll::enumContainers
author: windows-sdk-content
description: Retrieves the names of containers for the cryptographic service provider (CSP) specified by the ProviderName property. This method was first defined in the ICEnroll interface.
old-location: security\icenroll4_enumcontainers.htm
tech.root: SecCrypto
ms.assetid: 28102a55-3bda-4413-84b6-cfa2057be98b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],enumContainers method, ICEnroll interface [Security],enumContainers method, ICEnroll.enumContainers, ICEnroll2 interface [Security],enumContainers method, ICEnroll2::enumContainers, ICEnroll3 interface [Security],enumContainers method, ICEnroll3::enumContainers, ICEnroll4 interface [Security],enumContainers method, ICEnroll4::enumContainers, ICEnroll::enumContainers, enumContainers, enumContainers method [Security], enumContainers method [Security],CEnroll object, enumContainers method [Security],ICEnroll interface, enumContainers method [Security],ICEnroll2 interface, enumContainers method [Security],ICEnroll3 interface, enumContainers method [Security],ICEnroll4 interface, security.icenroll4_enumcontainers, xenroll/ICEnroll2::enumContainers, xenroll/ICEnroll3::enumContainers, xenroll/ICEnroll4::enumContainers, xenroll/ICEnroll::enumContainers
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.enumContainers
 - ICEnroll3.enumContainers
 - ICEnroll2.enumContainers
 - ICEnroll.enumContainers
 - CEnroll.enumContainers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::enumContainers


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumContainers</b> method retrieves the names of containers for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) specified by the 
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property. This method was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the container whose name will be retrieved. Specify zero for the first container.


### -param pbstr [out]

A pointer to a <b>BSTR</b> variable that receives the name of the container. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more items.

<h3>VB</h3>
 The return value is a <b>String</b> variable that represents the name of the container. An exception is raised if an error is encountered or when there are no more items.




## -remarks



If the 
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property value has not been set, the default value (usually Microsoft Base Cryptographic Provider) of <b>ProviderName</b> as set in the registry, is used.

This method is disabled when  the Certificate Enrollment Control is executed as a scripted control.


#### Examples


```cpp
BSTR       bstrCon = NULL;
DWORD      nCon = 0;
HRESULT    hr;

// pEnroll is previously instantiated ICEnroll interface pointer
while ( S_OK == pEnroll->enumContainers(nCon, &bstrCon) )
{
    printf("\t%d) %ws\n", nCon++, bstrCon );
    if ( bstrCon )
    {
        SysFreeString( bstrCon );
        bstrCon = NULL;
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a>
 

 

