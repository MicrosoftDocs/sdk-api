---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetDevicePath
title: IEnhancedStorageSilo::GetDevicePath method
author: windows-driver-content
description: Retrieves the path to the silo device node. The returned string is suitable for passing to Windows System APIs such as CreateFile or SetupDiOpenDeviceInterface.
old-location: enstor\ienhancedstoragesilo_getdevicepath.htm
old-project: enstor
ms.assetid: 98ef04a1-d14d-4de3-b24a-0f044335d75b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetDevicePath method [Enhanced Storage], GetDevicePath method [Enhanced Storage], IEnhancedStorageSilo interface, GetDevicePath,IEnhancedStorageSilo.GetDevicePath, IEnhancedStorageSilo, IEnhancedStorageSilo interface [Enhanced Storage], GetDevicePath method, IEnhancedStorageSilo::GetDevicePath, ehstorapi/IEnhancedStorageSilo::GetDevicePath, enstor.ienhancedstoragesilo_getdevicepath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EhStorAPI.h
api_name:
-	IEnhancedStorageSilo.GetDevicePath
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageSilo::GetDevicePath method


## -description


Retrieves the path to the silo device node. The returned string is suitable for passing to <b>Windows System</b> APIs such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or <a href="http://go.microsoft.com/fwlink/p/?linkid=134840">SetupDiOpenDeviceInterface</a>.


## -parameters




### -param ppwszSiloDevicePath [out]

A pointer to a string that represents the path to the Silo device node.


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
Device path string was retrieved successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszSiloDevicePath</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The memory to contain the device path string is allocated by the Enhanced Storage API and must be freed  by passing the  returned pointer to <a href="http://go.microsoft.com/fwlink/p/?linkid=134839">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

