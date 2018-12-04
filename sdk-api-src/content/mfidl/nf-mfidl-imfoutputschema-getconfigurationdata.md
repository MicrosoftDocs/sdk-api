---
UID: NF:mfidl.IMFOutputSchema.GetConfigurationData
title: IMFOutputSchema::GetConfigurationData
author: windows-sdk-content
description: Returns configuration data for the output protection system. The configuration data is used to enable or disable the protection system, and to set the protection levels.
old-location: mf\imfoutputschema_getconfigurationdata.htm
tech.root: medfound
ms.assetid: 26730d2d-8ebc-441b-a262-db0c8fe7e75a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 26730d2d-8ebc-441b-a262-db0c8fe7e75a, GetConfigurationData, GetConfigurationData method [Media Foundation], GetConfigurationData method [Media Foundation],IMFOutputSchema interface, IMFOutputSchema interface [Media Foundation],GetConfigurationData method, IMFOutputSchema.GetConfigurationData, IMFOutputSchema::GetConfigurationData, mf.imfoutputschema_getconfigurationdata, mfidl/IMFOutputSchema::GetConfigurationData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputSchema.GetConfigurationData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFOutputSchema::GetConfigurationData


## -description



Returns configuration data for the output protection system. The configuration data is used to enable or disable the protection system, and to set the protection levels.




## -parameters




### -param pdwVal [out]

Receives the configuration data. The meaning of this data depends on the output protection system.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d0786628-dde9-43a9-8e81-0b0c396ad426">IMFOutputSchema</a>
 

 

