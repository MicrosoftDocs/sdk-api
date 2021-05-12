---
UID: NF:msinkaut.IInkRecognizers.GetDefaultRecognizer
title: IInkRecognizers::GetDefaultRecognizer (msinkaut.h)
description: Retrieves the default recognizer for a known language, specified by a national language support (NLS) language code identifier (LCID).
helpviewer_keywords: ["499a257d-72de-4121-a98f-c827a3fef611","GetDefaultRecognizer","GetDefaultRecognizer method [Tablet PC]","GetDefaultRecognizer method [Tablet PC]","IInkRecognizers interface","IInkRecognizers interface [Tablet PC]","GetDefaultRecognizer method","IInkRecognizers.GetDefaultRecognizer","IInkRecognizers::GetDefaultRecognizer","msinkaut/IInkRecognizers::GetDefaultRecognizer","tablet.inkrecognizers_getdefaultrecognizer"]
old-location: tablet\inkrecognizers_getdefaultrecognizer.htm
tech.root: tablet
ms.assetid: 499a257d-72de-4121-a98f-c827a3fef611
ms.date: 12/05/2018
ms.keywords: 499a257d-72de-4121-a98f-c827a3fef611, GetDefaultRecognizer, GetDefaultRecognizer method [Tablet PC], GetDefaultRecognizer method [Tablet PC],IInkRecognizers interface, IInkRecognizers interface [Tablet PC],GetDefaultRecognizer method, IInkRecognizers.GetDefaultRecognizer, IInkRecognizers::GetDefaultRecognizer, msinkaut/IInkRecognizers::GetDefaultRecognizer, tablet.inkrecognizers_getdefaultrecognizer
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizers::GetDefaultRecognizer
 - msinkaut/IInkRecognizers::GetDefaultRecognizer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizers.GetDefaultRecognizer
---

# IInkRecognizers::GetDefaultRecognizer


## -description

Retrieves the default recognizer for a known language, specified by a national language support (NLS) language code identifier (LCID).

## -parameters

### -param lcid [in]

 The LCID locale identifier of the language for which you are retrieving the default recognizer. If <i>lcid</i> is 0, the method uses the user's locale setting to determine which default recognizer to retrieve. If the user has not specified a locale in Regional Options, the method uses the locale that was specified for the computer. The default value is 0.

### -param DefaultRecognizer [out, retval]

When this method returns, contains a pointer to the requested recognizer.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>

## -remarks

Each language can have a default recognizer. For example, a user can have a default recognizer for U.S. English and a default recognizer for French. If no locale is specified, this method returns the recognizer for the active input locale. To select the active input locale, in the Regional and Language Options in ControlPanel, on the Languages tab, users click Details, and then select the Default input language.

The default value of the <i>lcid</i> parameter is 0.

This method generates an error if the <i>lcid</i> parameter is not a known locale or if a recognizer is not installed for the requested locale.

<b>GetDefaultRecognizer</b> first checks if there is a matching recognizer for the user's input locale. If there is none, it checks if there is a matching recognizer for the current system locale.

For more information about NLS, see <a href="/windows/desktop/Intl/nls-terminology">NLS Terminology</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizers.md">IInkRecognizers</a>



<a href="/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)">InkRecognizers Collection</a>
