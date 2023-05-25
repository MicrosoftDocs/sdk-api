---
UID: NN:wmsdkidl.IWMLanguageList
title: IWMLanguageList (wmsdkidl.h)
description: The IWMLanguageList interface manages a list of languages supported by an ASF file.
helpviewer_keywords: ["IWMLanguageList","IWMLanguageList interface [windows Media Format]","IWMLanguageList interface [windows Media Format]","described","IWMLanguageListInterface","wmformat.iwmlanguagelist","wmsdkidl/IWMLanguageList"]
old-location: wmformat\iwmlanguagelist.htm
tech.root: wmformat
ms.assetid: 63ef282c-d1ab-4ce9-a56b-209407c7839b
ms.date: 4/26/2023
ms.keywords: IWMLanguageList, IWMLanguageList interface [windows Media Format], IWMLanguageList interface [windows Media Format],described, IWMLanguageListInterface, wmformat.iwmlanguagelist, wmsdkidl/IWMLanguageList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMLanguageList
 - wmsdkidl/IWMLanguageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMLanguageList
---

# IWMLanguageList interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMLanguageList</b> interface manages a list of languages supported by an ASF file. This interface supports both content and metadata in multiple languages.

The <b>IWMLanguageList</b> interface is supported in the profile, writer, metadata editor, reader, and synchronous reader objects. A pointer to an instance of <b>IWMLanguageList</b> can be obtained by calling the <b>QueryInterface</b> method of any interface in one of the listed objects.

<div class="alert"><b>Important</b>  Do not use this interface before opening the reader object.</div>
<div> </div>

## -inheritance

The <b>IWMLanguageList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLanguageList</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

This interface provides support for referencing languages by a string compliant with RFC 1766 – Tags for the Identification of Languages. Other interfaces in this SDK refer to the languages supported in an ASF file by language index. A language index is assigned to every language added to the language list.

This interface manages the list of languages supported for the file. Individual features of the file may not support all of the languages in the list. When selecting a language for playback of an output associated with a set of streams that are mutually exclusive by language, you must get the languages that are supported in that mutual exclusion object. You can retrieve the languages supported for a particular output by using the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4</a> interface.

When using this interface to add metadata in multiple languages to an MP3 file, only the first half of the language string is important. For example, the RFC 1766 identifier "en-us" designates English in the region of the United States. When written to an MP3 file, the identifier would be "en" without a regional designation.

For a list of common RFC 1766-compliant language identifiers, see <a href="/windows/desktop/wmformat/language-strings">Language Strings</a>.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="/windows/desktop/wmformat/profile-object">Profile Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
