---
UID: NN:wmsdkidl.IWMLanguageList
title: IWMLanguageList (wmsdkidl.h)
description: The IWMLanguageList interface manages a list of languages supported by an ASF file.helpviewer_keywords: ["IWMLanguageList","IWMLanguageList interface [windows Media Format]","IWMLanguageList interface [windows Media Format]","described","IWMLanguageListInterface","wmformat.iwmlanguagelist","wmsdkidl/IWMLanguageList"]
old-location: wmformat\iwmlanguagelist.htm
tech.root: wmformat
ms.assetid: 63ef282c-d1ab-4ce9-a56b-209407c7839b
ms.date: 12/05/2018
ms.keywords: IWMLanguageList, IWMLanguageList interface [windows Media Format], IWMLanguageList interface [windows Media Format],described, IWMLanguageListInterface, wmformat.iwmlanguagelist, wmsdkidl/IWMLanguageList
f1_keywords:
- wmsdkidl/IWMLanguageList
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMLanguageList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMLanguageList interface


## -description



The <b>IWMLanguageList</b> interface manages a list of languages supported by an ASF file. This interface supports both content and metadata in multiple languages.

The <b>IWMLanguageList</b> interface is supported in the profile, writer, metadata editor, reader, and synchronous reader objects. A pointer to an instance of <b>IWMLanguageList</b> can be obtained by calling the <b>QueryInterface</b> method of any interface in one of the listed objects.

<div class="alert"><b>Important</b>  Do not use this interface before opening the reader object.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMLanguageList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLanguageList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string">AddLanguageByRFC1766String</a>
</td>
<td align="left" width="63%">
Adds an entry to the list of supported languages for a file based upon a language tag compliant with RFC 1766.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount">GetLanguageCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of supported languages in the language list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails">GetLanguageDetails</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) and RFC 1766-compliant tag for an entry in the list of supported languages.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



This interface provides support for referencing languages by a string compliant with RFC 1766 – Tags for the Identification of Languages. Other interfaces in this SDK refer to the languages supported in an ASF file by language index. A language index is assigned to every language added to the language list.

This interface manages the list of languages supported for the file. Individual features of the file may not support all of the languages in the list. When selecting a language for playback of an output associated with a set of streams that are mutually exclusive by language, you must get the languages that are supported in that mutual exclusion object. You can retrieve the languages supported for a particular output by using the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4</a> interface.

When using this interface to add metadata in multiple languages to an MP3 file, only the first half of the language string is important. For example, the RFC 1766 identifier "en-us" designates English in the region of the United States. When written to an MP3 file, the identifier would be "en" without a regional designation.

For a list of common RFC 1766-compliant language identifiers, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/language-strings">Language Strings</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-object">Profile Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

