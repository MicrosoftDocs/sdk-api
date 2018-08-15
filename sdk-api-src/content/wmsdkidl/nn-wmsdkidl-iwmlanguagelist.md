---
UID: NN:wmsdkidl.IWMLanguageList
title: IWMLanguageList
author: windows-sdk-content
description: The IWMLanguageList interface manages a list of languages supported by an ASF file.
old-location: wmformat\iwmlanguagelist.htm
old-project: wmformat
ms.assetid: 63ef282c-d1ab-4ce9-a56b-209407c7839b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMLanguageList, IWMLanguageList interface [windows Media Format], IWMLanguageList interface [windows Media Format],described, IWMLanguageListInterface, wmformat.iwmlanguagelist, wmsdkidl/IWMLanguageList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMLanguageList
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMLanguageList interface


## -description



The <b>IWMLanguageList</b> interface manages a list of languages supported by an ASF file. This interface supports both content and metadata in multiple languages.

The <b>IWMLanguageList</b> interface is supported in the profile, writer, metadata editor, reader, and synchronous reader objects. A pointer to an instance of <b>IWMLanguageList</b> can be obtained by calling the <b>QueryInterface</b> method of any interface in one of the listed objects.

<div class="alert"><b>Important</b>  Do not use this interface before opening the reader object.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMLanguageList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMLanguageList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMLanguageList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aec575c-8e04-4252-8863-1a458e56dcef">AddLanguageByRFC1766String</a>
</td>
<td align="left" width="63%">
Adds an entry to the list of supported languages for a file based upon a language tag compliant with RFC 1766.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81c2edae-a793-421b-9aa2-39e280c43aeb">GetLanguageCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of supported languages in the language list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beb9f4fb-0acf-4693-b98e-2c197b330de5">GetLanguageDetails</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) and RFC 1766-compliant tag for an entry in the list of supported languages.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



This interface provides support for referencing languages by a string compliant with RFC 1766 – Tags for the Identification of Languages. Other interfaces in this SDK refer to the languages supported in an ASF file by language index. A language index is assigned to every language added to the language list.

This interface manages the list of languages supported for the file. Individual features of the file may not support all of the languages in the list. When selecting a language for playback of an output associated with a set of streams that are mutually exclusive by language, you must get the languages that are supported in that mutual exclusion object. You can retrieve the languages supported for a particular output by using the methods of the <a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4</a> interface.

When using this interface to add metadata in multiple languages to an MP3 file, only the first half of the language string is important. For example, the RFC 1766 identifier "en-us" designates English in the region of the United States. When written to an MP3 file, the identifier would be "en" without a regional designation.

For a list of common RFC 1766-compliant language identifiers, see <a href="https://msdn.microsoft.com/625f7e95-0d21-4e16-8323-0f6301a04b30">Language Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/ec42889e-580e-4a65-9fe6-4a5f15c97eb0">Profile Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

