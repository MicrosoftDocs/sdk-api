---
UID: NF:msctf.ITfContextOwner.GetAttribute
title: ITfContextOwner::GetAttribute
author: windows-sdk-content
description: The ITfContextOwner::GetAttribute method returns the value of a supported attribute. If the attribute is unsupported, the pvarValue parameter is set to VT_EMPTY.
old-location: tsf\itfcontextowner_getattribute.htm
old-project: TSF
ms.assetid: a249d529-fdb1-4f5f-84ae-f26dae917609
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAttribute, GetAttribute method [Text Services Framework], GetAttribute method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetAttribute method, ITfContextOwner.GetAttribute, ITfContextOwner::GetAttribute, _tsf_itfcontextowner_getattribute_ref, msctf/ITfContextOwner::GetAttribute, tsf.itfcontextowner_getattribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: Msimtf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextOwner::GetAttribute


## -description


The <b>ITfContextOwner::GetAttribute</b> method returns the value of a supported attribute. If the attribute is unsupported, the <i>pvarValue</i> parameter is set to VT_EMPTY.


## -parameters




### -param rguidAttribute [in]

Specifies the attribute GUID.


### -param pvarValue [out]

Receives the attribute value. If the attribute is unsupported, this parameter is set to VT_EMPTY.


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
 




## -remarks



Context owners using the default text store of the TSF manager can implement a simplified version of attributes with this method. The supported attributes are application or text service dependent. For more information about predefined attributes recognized in TSF, see the following topics.




## -see-also




<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/8536938b-98a1-415b-b5f2-45b90215c270">Other Predefined Attributes</a>



<a href="https://msdn.microsoft.com/8d73c258-77d5-46db-9d31-ac41d9e7acb3">Predefined Font Attributes</a>



<a href="https://msdn.microsoft.com/9a9e1912-51c0-40e0-9e3a-b84ea7077dbe">Predefined List Attributes</a>



<a href="https://msdn.microsoft.com/af73edb8-b706-40e4-a093-4ac22d33ecdc">Predefined Text Attributes</a>
 

 

