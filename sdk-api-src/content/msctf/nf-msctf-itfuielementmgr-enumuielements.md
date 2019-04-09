---
UID: NF:msctf.ITfUIElementMgr.EnumUIElements
title: ITfUIElementMgr::EnumUIElements (msctf.h)
author: windows-sdk-content
description: The ITfUIElementMgr::EnumUIElements method returns IEnumTfUIElements interface pointer to enumerate the ITfUIElement.
old-location: tsf\itfuielementmgr_enumuielements.htm
tech.root: TSF
ms.assetid: cdede376-be18-4deb-ae79-594aebb085a6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumUIElements, EnumUIElements method [Text Services Framework], EnumUIElements method [Text Services Framework],ITfUIElementMgr interface, ITfUIElementMgr interface [Text Services Framework],EnumUIElements method, ITfUIElementMgr.EnumUIElements, ITfUIElementMgr::EnumUIElements, msctf/ITfUIElementMgr::EnumUIElements, tsf.itfuielementmgr_enumuielements
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - Msctf.dll
api_name:
 - ITfUIElementMgr.EnumUIElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfUIElementMgr::EnumUIElements


## -description


The <b>ITfUIElementMgr::EnumUIElements</b> method returns <a href="https://msdn.microsoft.com/5ee3d89c-0761-4d4b-9fd9-6b9de7ceb077">IEnumTfUIElements</a> interface pointer to enumerate the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a>.


## -parameters




### -param ppEnum [in]

[in] A pointer to receive the <a href="https://msdn.microsoft.com/5ee3d89c-0761-4d4b-9fd9-6b9de7ceb077">IEnumTfUIElements</a> interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



