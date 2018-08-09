---
UID: NF:wmsdkidl.IWMProfileManagerLanguage.GetUserLanguageID
title: IWMProfileManagerLanguage::GetUserLanguageID
author: windows-sdk-content
description: The GetUserLanguageID method retrieves the language identifier for the system profiles loaded by the profile manager object.
old-location: wmformat\iwmprofilemanagerlanguage_getuserlanguageid.htm
old-project: wmformat
ms.assetid: 92d18ac9-8f68-47c6-91d7-de7653df69a6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetUserLanguageID, GetUserLanguageID method [windows Media Format], GetUserLanguageID method [windows Media Format],IWMProfileManagerLanguage interface, IWMProfileManagerLanguage interface [windows Media Format],GetUserLanguageID method, IWMProfileManagerLanguage.GetUserLanguageID, IWMProfileManagerLanguage::GetUserLanguageID, IWMProfileManagerLanguageGetUserLanguageID, wmformat.iwmprofilemanagerlanguage_getuserlanguageid, wmsdkidl/IWMProfileManagerLanguage::GetUserLanguageID
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
 - IWMProfileManagerLanguage.GetUserLanguageID
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManagerLanguage::GetUserLanguageID


## -description



The <b>GetUserLanguageID</b> method retrieves the language identifier for the system profiles loaded by the profile manager object.




## -parameters




### -param wLangID [out]

Pointer to a <b>WORD</b> that receives the language identifier (LANGID) of the language set in the profile manager.


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



The default language is U.S. English (0x409).




## -see-also




<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage Interface</a>



<a href="https://msdn.microsoft.com/e2154057-ea76-43bb-92d9-b52f16eb6b1b">IWMProfileManagerLanguage::SetUserLanguageID</a>



<a href="https://msdn.microsoft.com/2c218ab4-ecdb-414c-aa42-b71a42e340e5">Localized System Profiles</a>



<a href="https://msdn.microsoft.com/d911baf6-0731-4f02-9001-d04464a03f56">Working with Localized System Profiles</a>
 

 

