---
UID: NF:combaseapi.CoGetTreatAsClass
title: CoGetTreatAsClass function
author: windows-sdk-content
description: Returns the CLSID of an object that can emulate the specified object.
old-location: com\cogettreatasclass.htm
tech.root: com
ms.assetid: f95fefe6-dc37-45f4-93be-87c996990ab9
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CoGetTreatAsClass, CoGetTreatAsClass function [COM], _com_CoGetTreatAsClass, com.cogettreatasclass, combaseapi/CoGetTreatAsClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetTreatAsClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetTreatAsClass function


## -description


Returns the CLSID of an object that can emulate the specified object.




## -parameters




### -param clsidOld [in]

The CLSID of the object that can be emulated (treated as) an object with a different CLSID.


### -param pClsidNew [out]

A pointer to where the CLSID that can emulate <i>clsidOld</i> objects is retrieved. This parameter cannot be <b>NULL</b>. If there is no emulation information for <i>clsidOld</i> objects, the <i>clsidOld</i> parameter is supplied.


## -returns



This function can return the following values, as well as any error values returned by the <a href="https://msdn.microsoft.com/en-us/library/ms680589(v=VS.85).aspx">CLSIDFromString</a> function.

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
A new CLSID was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no emulation information for the <i>clsidOld</i> parameter, so the <i>pClsidNew</i> parameter is set to <i>clsidOld</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB </b></dt>
</dl>
</td>
<td width="60%">
There was an error reading the registry.

</td>
</tr>
</table>
 




## -remarks



<b>CoGetTreatAsClass</b> returns the <a href="https://msdn.microsoft.com/1d7a1677-738a-4258-9afc-e77bd0dcf40f">TreatAs</a> entry in the registry for the specified object. The <b>TreatAs</b> entry, if set, is the CLSID of a registered object (an application) that can emulate the object in question. The <b>TreatAs</b> entry is set through a call to the <a href="https://msdn.microsoft.com/en-us/library/ms693452(v=VS.85).aspx">CoTreatAsClass</a> function. Emulation allows an application to open and edit an object of a different format, while retaining the original format of the object. Objects of the original CLSID are activated and treated as objects of the second CLSID. When the object is saved, this may result in loss of edits not supported by the original format. If there is no <b>TreatAs</b> entry for the specified object, this function returns the CLSID of the original object (<i>clsidOld</i>). 





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693452(v=VS.85).aspx">CoTreatAsClass</a>
 

 

