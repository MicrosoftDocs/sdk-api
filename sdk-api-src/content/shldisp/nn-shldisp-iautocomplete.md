---
UID: NN:shldisp.IAutoComplete
title: IAutoComplete
author: windows-sdk-content
description: Exposed by the autocomplete object (CLSID_AutoComplete). This interface allows applications to initialize, enable, and disable the object.
old-location: shell\IAutoComplete.htm
old-project: shell
ms.assetid: bed6eb41-3086-4af7-8c75-651da9dba3b2
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IAutoComplete, IAutoComplete interface [Windows Shell], IAutoComplete interface [Windows Shell],described, _win32_IAutoComplete, shell.IAutoComplete, shldisp/IAutoComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IAutoComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IAutoComplete interface


## -description


Exposed by the autocomplete object (CLSID_AutoComplete). This interface allows applications to initialize, enable, and disable the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutoComplete</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAutoComplete</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAutoComplete</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables autocompletion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the autocomplete object.

</td>
</tr>
</table> 


## -remarks



Autocompletion expands strings that have been partially entered in an <a href="https://msdn.microsoft.com/library/Bb775458(v=VS.85).aspx">edit control</a> into complete strings. For example, when a user starts to type a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URLs that are consistent with the existing partial string. A partial URL string such as "mic" might be expanded to "http://www.microsoft.com" or "http://www.microsoft.com/windows". Autocompletion is typically used with edit controls or with controls that have an embedded edit control such as the <a href="https://msdn.microsoft.com/library/Bb775740(v=VS.85).aspx">comboboxex control</a>.

Autocompletion has two modes for displaying the completed string. The modes are independent, so you can enable either or both. To specify the mode, call <a href="https://msdn.microsoft.com/d3562845-fc28-4726-a520-29720f9924fc">IAutoComplete2::SetOptions</a>. The modes are as follows:
				

<ul>
<li>In <i>autoappend</i> mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters. The edit control behaves as if the user had entered the entire string manually and then highlighted the appended characters. If the user continues to enter characters, they are added to the existing partial string. If the user adds a character that is identical to the next highlighted character, the highlighting for that character will be turned off. The remaining characters will still be highlighted. If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string. It appends the remainder of the new candidate string to the current partial string, as before. If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion. This process continues until the user accepts a string.</li>
<li>In <i>autosuggest</i> mode, autocompletion displays a drop-down list beneath the edit control with one or more suggested complete strings. The user can select one of the suggested strings, usually by clicking it, or continue typing. As typing progresses, the drop-down list may be modified, based on the current partial string. If you set the <b>ACO_SEARCH</b> flag in the <i>dwFlag</i> parameter of <a href="https://msdn.microsoft.com/d3562845-fc28-4726-a520-29720f9924fc">IAutoComplete2::SetOptions</a>, a "Search for 'XXX'" item is added to the bottom of the drop-down list. It is displayed even if there are no suggested strings. "XXX" is set to the current partial string and is updated as the user continues to type. If the user selects "Search for '...'", your application should launch a search engine to assist the user.</li>
</ul>
The simplest way to implement autocompletion is to call <a href="https://msdn.microsoft.com/b47efa8d-2118-4805-bb04-97bd143228dc">SHAutoComplete</a>. When this function is called for a system edit control, the control will autocomplete partially entered file system paths or URLs. To enable autocompletion for other types of strings, or to have more control over how autocompletion works, you can use the underlying autocomplete object directly.

This interface is not usually implemented by applications. It is exposed by the Shell's autocomplete object and used by applications.

Use the <b>IAutoComplete</b> interface of the autocomplete object to initialize the object and to 
enable or disable autocompletion.

To implement autocompletion for an edit control using the autocomplete object, do the following:
				

<ol>
<li>Implement a string list Component Object Model (COM) object that exports an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface. This string list object is responsible for providing the list of strings that the autocomplete object will use as candidates for completed strings.</li>
<li>Create an instance of the autocomplete object with <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>. Request a pointer to its <b>IAutoComplete</b> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/e5ee36b7-11b4-4eca-ae8e-eefa6245f287">IAutoComplete::Init</a>. Set the <i>hwndEdit</i> parameter to the window handle of the edit control. If the edit control is embedded in another control, you must retrieve the handle to the edit control itself. For example, to retrieve a handle to the edit control embedded in a <a href="https://msdn.microsoft.com/library/Bb775740(v=VS.85).aspx">comboboxex control</a>, send a <a href="https://msdn.microsoft.com/library/Bb775772(v=VS.85).aspx">CBEM_GETEDITCONTROL</a> message. Set the <i>punkACL</i> parameter of <b>IAutoComplete::Init</b> to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer of the string list object.</li>
<li>If you do not want to use the default options, retrieve a pointer to the autocomplete object's <a href="https://msdn.microsoft.com/c093719f-7176-4ba4-ae75-399e8beeebf0">IAutoComplete2</a> interface. Call <a href="https://msdn.microsoft.com/d3562845-fc28-4726-a520-29720f9924fc">IAutoComplete2::SetOptions</a> to set the desired options.</li>
<li>The autocomplete object uses the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer of the string list object, passed as <i>punkACL</i> in step 3, to retrieve a pointer to that object's <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface. The autocomplete object then calls that interface to generate its list of candidate strings. It selects strings from that list that are an acceptable match to the partial string in the control. In autoappend mode, the characters needed to complete the string are appended to the partial string and highlighted. In autosuggest mode, a drop-down box with a list of one or more possible strings is displayed below the edit control.</li>
<li>If the user accepts an autocompleted string, the edit control behaves as if the string had been entered manually.</li>
</ol>
Autocompletion is enabled by default. Applications need only to call <a href="https://msdn.microsoft.com/dd22d855-6ade-4e30-9d39-a4a6434e7185">IAutoComplete::Enable</a> to disable autocompletion or to reenable it if it has been disabled.




## -see-also




<a href="https://msdn.microsoft.com/66513683-38ca-4b19-88d5-d14bf7ae73eb">IACList</a>



<a href="https://msdn.microsoft.com/b765c9dd-20e9-428f-877a-aff4fac44664">IACList2</a>



<a href="https://msdn.microsoft.com/c093719f-7176-4ba4-ae75-399e8beeebf0">IAutoComplete2</a>



<a href="https://msdn.microsoft.com/1fdbe616-3ca3-4f07-b89c-4c76561ba169">ICurrentWorkingDirectory</a>



<a href="https://msdn.microsoft.com/c0556a87-2be5-43dc-9ca6-dfbdae7e7137">IObjMgr</a>
 

 

