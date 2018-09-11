---
UID: NF:spellcheckprovider.ISpellCheckProvider.InitializeWordlist
title: ISpellCheckProvider::InitializeWordlist
author: windows-sdk-content
description: Initialize the specified word list to contain only the specified words.
old-location: intl\ispellcheckprovider_initializewordlist.htm
tech.root: Intl
ms.assetid: B1E3D0F9-8A6B-431F-A8AF-46D783E23FEF
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ISpellCheckProvider interface [Internationalization for Windows Applications],InitializeWordlist method, ISpellCheckProvider.InitializeWordlist, ISpellCheckProvider::InitializeWordlist, InitializeWordlist, InitializeWordlist method [Internationalization for Windows Applications], InitializeWordlist method [Internationalization for Windows Applications],ISpellCheckProvider interface, intl.ispellcheckprovider_initializewordlist, spellcheckprovider/ISpellCheckProvider::InitializeWordlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheckprovider.idl
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
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProvider.InitializeWordlist
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProvider::InitializeWordlist


## -description


Initialize the specified word list to contain only the specified words.


## -parameters




### -param wordlistType [in]

The type of word list.


### -param words [in]

The set of words to be included in the word list, passed as an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> object..


## -returns



This method can return one of these values.

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
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wordlistType</i> is not a valid member of the <a href="https://msdn.microsoft.com/F1D517F3-CAE3-46DC-867E-D8D73C20CF9A">WORDLIST_TYPE</a> enumeration.

</td>
</tr>
</table>
 




## -remarks



This method is called by the system (for example, when the client calls <a href="https://msdn.microsoft.com/d600a57e-7191-4a82-8004-026a04ef94ed">ISpellChecker::Add</a>), which passes the words from the respective word list to the provider so that it can consider the word list when spell checking.




## -see-also




<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>



<a href="https://msdn.microsoft.com/d600a57e-7191-4a82-8004-026a04ef94ed">ISpellChecker::Add</a>



<a href="https://msdn.microsoft.com/F1D517F3-CAE3-46DC-867E-D8D73C20CF9A">WORDLIST_TYPE</a>
 

 

