---
UID: NF:dsclient.IDsDisplaySpecifier.GetDisplaySpecifier
title: IDsDisplaySpecifier::GetDisplaySpecifier
author: windows-sdk-content
description: The IDsDisplaySpecifier::GetDisplaySpecifier method binds to the display specifier object for a given class in Active Directory Domain Services.
old-location: ad\idsdisplayspecifier_getdisplayspecifier.htm
tech.root: ad
ms.assetid: c4fc25f6-0157-406d-b523-8542183291ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDisplaySpecifier, GetDisplaySpecifier method [Active Directory], GetDisplaySpecifier method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetDisplaySpecifier method, IDsDisplaySpecifier.GetDisplaySpecifier, IDsDisplaySpecifier::GetDisplaySpecifier, _glines_idsdisplayspecifier_getdisplayspecifier, ad.idsdisplayspecifier__getdisplayspecifier, ad.idsdisplayspecifier_getdisplayspecifier, dsclient/IDsDisplaySpecifier::GetDisplaySpecifier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsclient.h
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
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetDisplaySpecifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::GetDisplaySpecifier


## -description


The <b>IDsDisplaySpecifier::GetDisplaySpecifier</b> method binds to the display specifier object for a given class in Active Directory Domain Services.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to retrieve the display specifier   for.


### -param riid [in]

Contains the interface identifier of the desired interface.


### -param ppv [in, out]

Pointer to an interface pointer that receives the display specifier of the object class.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -remarks



This method uses the 
<a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a> function to bind to the display specifier object of the given class. If that fails, it attempts to bind to the display specifier in the user locale. If this fails again, it binds to the display specifier in the default locale.

This method uses the server and user credentials set by a previous call to 
<a href="https://msdn.microsoft.com/f72cc711-7dec-4f5a-9cf1-57612240b435">IDsDisplaySpecifier::SetServer</a>.


#### Examples

The following code example demonstrates how to call this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IDsDisplaySpecifier *pDS;

hr = CoCreateInstance(CLSID_DsDisplaySpecifier,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IDsDisplaySpecifier,
                        (void**)&amp;pDS);
if(SUCCEEDED(hr))
{
    IADs *pads;

    hr = pDS-&gt;GetDisplaySpecifier(L"user", IID_IADs, (LPVOID*)&amp;pads);

    if(SUCCEEDED(hr))
    {
        pads-&gt;Release();
    }

    pDS-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>



<a href="https://msdn.microsoft.com/f72cc711-7dec-4f5a-9cf1-57612240b435">IDsDisplaySpecifier::SetServer</a>
 

 

