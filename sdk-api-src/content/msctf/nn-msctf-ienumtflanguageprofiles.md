---
UID: NN:msctf.IEnumTfLanguageProfiles
title: IEnumTfLanguageProfiles
author: windows-sdk-content
description: The IEnumTfLanguageProfiles interface is implemented by the TSF manager to provide an enumeration of language profiles.
old-location: tsf\ienumtflanguageprofiles.htm
tech.root: TSF
ms.assetid: 8ac41bff-8537-4558-a92c-6e7dae6a6bdf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IEnumTfLanguageProfiles, IEnumTfLanguageProfiles interface [Text Services Framework], IEnumTfLanguageProfiles interface [Text Services Framework],described, _tsf_ienumtflanguageprofiles_ref, msctf/IEnumTfLanguageProfiles, tsf.ienumtflanguageprofiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfLanguageProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfLanguageProfiles interface


## -description


The <b>IEnumTfLanguageProfiles</b> interface is implemented by the TSF manager to provide an enumeration of language profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfLanguageProfiles</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfLanguageProfiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfLanguageProfiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77fbb195-b3c8-4254-a4d9-117ea8052951">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/790fb0f4-4abd-4947-8e9a-68739657a8f8">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30be7551-f326-4132-814a-a896b148f2fe">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67e6d841-a3e9-4e55-ac35-9197f256d9bf">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

