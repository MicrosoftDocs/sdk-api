---
UID: NF:winsync.ISingleItemException.GetClockVector
title: ISingleItemException::GetClockVector
author: windows-sdk-content
description: Gets the clock vector that is associated with the item exception.
old-location: winsync\isingleitemexception_getclockvector.htm
tech.root: winsync
ms.assetid: e212e561-9baa-46d0-90c0-ec143b24e641
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetClockVector, GetClockVector method [Windows Sync], GetClockVector method [Windows Sync],ISingleItemException interface, ISingleItemException interface [Windows Sync],GetClockVector method, ISingleItemException.GetClockVector, ISingleItemException::GetClockVector, winsync.isingleitemexception_getclockvector, winsync/ISingleItemException::GetClockVector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - COM
api_location:
 - winsync.h
api_name:
 - ISingleItemException.GetClockVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISingleItemException::GetClockVector


## -description


Gets the clock vector that is associated with the item exception.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumClockVector</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and represents the clock vector that is associated with this exception.



## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/623553cb-9dc2-4504-9c49-357a0526b130">ISingleItemException Interface</a>
 

 

