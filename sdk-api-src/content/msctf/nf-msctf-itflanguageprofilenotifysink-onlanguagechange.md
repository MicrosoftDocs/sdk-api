---
UID: NF:msctf.ITfLanguageProfileNotifySink.OnLanguageChange
title: ITfLanguageProfileNotifySink::OnLanguageChange
author: windows-sdk-content
description: ITfLanguageProfileNotifySink::OnLanguageChange method
old-location: tsf\itflanguageprofilenotifysink_onlanguagechange.htm
old-project: TSF
ms.assetid: 4367265b-892b-4f75-af23-e90327fb4144
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfLanguageProfileNotifySink interface [Text Services Framework],OnLanguageChange method, ITfLanguageProfileNotifySink.OnLanguageChange, ITfLanguageProfileNotifySink::OnLanguageChange, OnLanguageChange, OnLanguageChange method [Text Services Framework], OnLanguageChange method [Text Services Framework],ITfLanguageProfileNotifySink interface, _tsf_itflanguageprofilenotifysink_onlanguagechange_ref, msctf/ITfLanguageProfileNotifySink::OnLanguageChange, tsf.itflanguageprofilenotifysink_onlanguagechange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfLanguageProfileNotifySink.OnLanguageChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfLanguageProfileNotifySink::OnLanguageChange


## -description




## -parameters




### -param langid [in]

Contains a <b>LANGID</b> value the identifies the new language profile.


### -param pfAccept [out]

Pointer to a <b>BOOL</b> value that receives a flag that permits or prevents the language profile change. Receives zero to prevent the language profile change or nonzero to permit the language profile change.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 



