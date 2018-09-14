---
UID: NF:inputscope.ITfInputScope.GetXML
title: ITfInputScope::GetXML
author: windows-sdk-content
description: ITfInputScope::GetXML method
old-location: tsf\itfinputscope_getXML.htm
tech.root: TSF
ms.assetid: 7e7a2780-6080-4f9a-b036-bc8f6258bcb5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetXML, GetXML method [Text Services Framework], GetXML method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetXML method, ITfInputScope.GetXML, ITfInputScope::GetXML, inputscope/ITfInputScope::GetXML, tsf.itfinputscope_getXML, tsf.itfinputscope_xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
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
 - ITfInputScope.GetXML
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfInputScope::GetXML


## -description




## -parameters




### -param pbstrXML [out]

Pointer to a string containing the xml string. The calling function must call <b>SysFreeString()</b> to free the buffer.


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
 



