---
UID: NN:shldisp.IAutoComplete
title: IAutoComplete (shldisp.h)
description: Exposed by the autocomplete object (CLSID_AutoComplete). This interface allows applications to initialize, enable, and disable the object.
helpviewer_keywords: ["IAutoComplete","IAutoComplete interface [Windows Shell]","IAutoComplete interface [Windows Shell]","described","_win32_IAutoComplete","shell.IAutoComplete","shldisp/IAutoComplete"]
old-location: shell\IAutoComplete.htm
tech.root: shell
ms.assetid: bed6eb41-3086-4af7-8c75-651da9dba3b2
ms.date: 12/05/2018
ms.keywords: IAutoComplete, IAutoComplete interface [Windows Shell], IAutoComplete interface [Windows Shell],described, _win32_IAutoComplete, shell.IAutoComplete, shldisp/IAutoComplete
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutoComplete
 - shldisp/IAutoComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IAutoComplete
---

# IAutoComplete interface


## -description

Exposed by the autocomplete object (CLSID_AutoComplete). This interface allows applications to initialize, enable, and disable the object.

## -inheritance

The <b>IAutoComplete</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAutoComplete</b> also has these types of members:

## -remarks

Autocompletion expands strings that have been partially entered in an <a href="/windows/desktop/Controls/edit-controls">edit control</a> into complete strings. For example, when a user starts to type a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URLs that are consistent with the existing partial string. A partial URL string such as "mic" might be expanded to "http://www.microsoft.com" or "http://www.microsoft.com/windows". Autocompletion is typically used with edit controls or with controls that have an embedded edit control such as the <a href="/windows/desktop/Controls/comboboxex-control-reference">comboboxex control</a>.

Autocompletion has two modes for displaying the completed string. The modes are independent, so you can enable either or both. To specify the mode, call <a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-setoptions">IAutoComplete2::SetOptions</a>. The modes are as follows:
				

<ul>
<li>In <i>autoappend</i> mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters. The edit control behaves as if the user had entered the entire string manually and then highlighted the appended characters. If the user continues to enter characters, they are added to the existing partial string. If the user adds a character that is identical to the next highlighted character, the highlighting for that character will be turned off. The remaining characters will still be highlighted. If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string. It appends the remainder of the new candidate string to the current partial string, as before. If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion. This process continues until the user accepts a string.</li>
<li>In <i>autosuggest</i> mode, autocompletion displays a drop-down list beneath the edit control with one or more suggested complete strings. The user can select one of the suggested strings, usually by clicking it, or continue typing. As typing progresses, the drop-down list may be modified, based on the current partial string. If you set the <b>ACO_SEARCH</b> flag in the <i>dwFlag</i> parameter of <a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-setoptions">IAutoComplete2::SetOptions</a>, a "Search for 'XXX'" item is added to the bottom of the drop-down list. It is displayed even if there are no suggested strings. "XXX" is set to the current partial string and is updated as the user continues to type. If the user selects "Search for '...'", your application should launch a search engine to assist the user.</li>
</ul>
The simplest way to implement autocompletion is to call <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete">SHAutoComplete</a>. When this function is called for a system edit control, the control will autocomplete partially entered file system paths or URLs. To enable autocompletion for other types of strings, or to have more control over how autocompletion works, you can use the underlying autocomplete object directly.

This interface is not usually implemented by applications. It is exposed by the Shell's autocomplete object and used by applications.

Use the <b>IAutoComplete</b> interface of the autocomplete object to initialize the object and to 
enable or disable autocompletion.

To implement autocompletion for an edit control using the autocomplete object, do the following:
				

<ol>
<li>Implement a string list Component Object Model (COM) object that exports an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface. This string list object is responsible for providing the list of strings that the autocomplete object will use as candidates for completed strings.</li>
<li>Create an instance of the autocomplete object with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. Request a pointer to its <b>IAutoComplete</b> interface.</li>
<li>Call <a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete-init">IAutoComplete::Init</a>. Set the <i>hwndEdit</i> parameter to the window handle of the edit control. If the edit control is embedded in another control, you must retrieve the handle to the edit control itself. For example, to retrieve a handle to the edit control embedded in a <a href="/windows/desktop/Controls/comboboxex-control-reference">comboboxex control</a>, send a <a href="/windows/desktop/Controls/cbem-geteditcontrol">CBEM_GETEDITCONTROL</a> message. Set the <i>punkACL</i> parameter of <b>IAutoComplete::Init</b> to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of the string list object.</li>
<li>If you do not want to use the default options, retrieve a pointer to the autocomplete object's <a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2">IAutoComplete2</a> interface. Call <a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-setoptions">IAutoComplete2::SetOptions</a> to set the desired options.</li>
<li>The autocomplete object uses the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of the string list object, passed as <i>punkACL</i> in step 3, to retrieve a pointer to that object's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface. The autocomplete object then calls that interface to generate its list of candidate strings. It selects strings from that list that are an acceptable match to the partial string in the control. In autoappend mode, the characters needed to complete the string are appended to the partial string and highlighted. In autosuggest mode, a drop-down box with a list of one or more possible strings is displayed below the edit control.</li>
<li>If the user accepts an autocompleted string, the edit control behaves as if the string had been entered manually.</li>
</ol>
Autocompletion is enabled by default. Applications need only to call <a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete-enable">IAutoComplete::Enable</a> to disable autocompletion or to reenable it if it has been disabled.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist">IACList</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2">IACList2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2">IAutoComplete2</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory">ICurrentWorkingDirectory</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr">IObjMgr</a>
