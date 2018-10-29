---
UID: NF:mfobjects.IMFPluginControl.SetDisabled
title: IMFPluginControl::SetDisabled
author: windows-sdk-content
description: Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.
old-location: mf\imfplugincontrol_imfplugincontrol__setdisabled.htm
tech.root: medfound
ms.assetid: ff50e746-42f5-4fbe-a904-f83b3c691d32
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFPluginControl interface [Media Foundation],SetDisabled method, IMFPluginControl.SetDisabled, IMFPluginControl::SetDisabled, SetDisabled, SetDisabled method [Media Foundation], SetDisabled method [Media Foundation],IMFPluginControl interface, mf.imfplugincontrol_imfplugincontrol__setdisabled, mfobjects/IMFPluginControl::SetDisabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - mfobjects.h
api_name:
 - IMFPluginControl.SetDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPluginControl::SetDisabled


## -description


Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.


## -parameters




### -param pluginType [in]

Member of the <a href="https://msdn.microsoft.com/f967cf3f-582c-457a-ba75-980feb2d9bf3">MF_Plugin_Type</a> enumeration, specifying the type of object.


### -param clsid [in]

The CLSID to add or remove.


### -param disabled [in]

Specifies whether to add or remove the CSLID. If the value is <b>TRUE</b>, the method adds the CLSID to the blocked list. Otherwise, the method removes it from the list.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



The blocked list is global to the caller's process. Calling this method does not affect the list in other processes.
      




## -see-also




<a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>
 

 

