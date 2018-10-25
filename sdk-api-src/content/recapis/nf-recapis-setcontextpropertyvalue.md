---
UID: NF:recapis.SetContextPropertyValue
title: SetContextPropertyValue function
author: windows-sdk-content
description: Adds a property to the recognizer context.If a property already exists, its value is modified.
old-location: tablet\setcontextpropertyvalue.htm
tech.root: tablet
ms.assetid: 42b1857d-92ee-456f-aafc-b8780526a137
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 42b1857d-92ee-456f-aafc-b8780526a137, SetContextPropertyValue, SetContextPropertyValue function [Tablet PC], recapis/SetContextPropertyValue, tablet.setcontextpropertyvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - SetContextPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetContextPropertyValue function


## -description



Adds a property to the recognizer context.

If a property already exists, its value is modified.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pGuid

The property to set. Specify a predefined property globally unique identifier (GUID) or application-defined property GUID. For a list of predefined properties, see the recognition <a href="https://msdn.microsoft.com/dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e">Property GUIDs</a>.


### -param cbSize

The size, in bytes, of the <i>pProperty</i> buffer.


### -param pProperty

The buffer that contains the property value.


## -returns



This function can return one of these values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pGUID</i> is invalid or <i>cbSize</i> has been set to a very large, invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
<i>pGUID</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>cbSize</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned when an attempt is made to set a property value when it has already been enabled.

</td>
</tr>
</table>
 




## -remarks



The <b>SetContextPropertyValue</b> function is optional.




## -see-also




<a href="https://msdn.microsoft.com/3d3df56f-d989-4d3b-a0e2-00a7ac0fabd6">GetContextPropertyList Function</a>



<a href="https://msdn.microsoft.com/e3f154ce-b4bf-4520-a4de-03cfe27ef9b0">GetContextPropertyValue Function</a>
 

 

