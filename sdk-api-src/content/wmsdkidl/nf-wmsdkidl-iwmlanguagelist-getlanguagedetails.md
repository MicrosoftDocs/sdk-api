---
UID: NF:wmsdkidl.IWMLanguageList.GetLanguageDetails
title: IWMLanguageList::GetLanguageDetails
author: windows-sdk-content
description: The GetLanguageDetails method retrieves the RFC 1766-compliant language tag for an entry in the list of supported languages.
old-location: wmformat\iwmlanguagelist_getlanguagedetails.htm
old-project: wmformat
ms.assetid: beb9f4fb-0acf-4693-b98e-2c197b330de5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLanguageDetails, GetLanguageDetails method [windows Media Format], GetLanguageDetails method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],GetLanguageDetails method, IWMLanguageList.GetLanguageDetails, IWMLanguageList::GetLanguageDetails, IWMLanguageListGetLanguageDetails, wmformat.iwmlanguagelist_getlanguagedetails, wmsdkidl/IWMLanguageList::GetLanguageDetails
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMLanguageList.GetLanguageDetails
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMLanguageList::GetLanguageDetails


## -description



The <b>GetLanguageDetails</b> method retrieves the RFC 1766-compliant language tag for an entry in the list of supported languages.




## -parameters




### -param wIndex [in]

<b>WORD</b> containing the index in the language list.


### -param pwszLanguageString [out]

Pointer to the RFC 1766-compliant language tag of the language list entry specified by <i>wIndex</i>. Pass <b>NULL</b> to retrieve the length of the string, which will be returned in <i>pcbLanguageStringLength</i>.


### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the length of the language string, in wide characters. This length includes the terminating <b>null</b> character.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



For a list of common RFC 1766-compliant language identifiers, see <a href="https://msdn.microsoft.com/625f7e95-0d21-4e16-8323-0f6301a04b30">Language Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/63ef282c-d1ab-4ce9-a56b-209407c7839b">IWMLanguageList Interface</a>
 

 

