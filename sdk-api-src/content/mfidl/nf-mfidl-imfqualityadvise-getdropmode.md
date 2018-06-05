---
UID: NF:mfidl.IMFQualityAdvise.GetDropMode
title: IMFQualityAdvise::GetDropMode
author: windows-sdk-content
description: Retrieves the current drop mode.
old-location: mf\imfqualityadvise_getdropmode.htm
old-project: medfound
ms.assetid: bb700a3e-837f-4e88-a9b7-294c41143402
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetDropMode, GetDropMode method [Media Foundation], GetDropMode method [Media Foundation],IMFQualityAdvise interface, IMFQualityAdvise interface [Media Foundation],GetDropMode method, IMFQualityAdvise.GetDropMode, IMFQualityAdvise::GetDropMode, bb700a3e-837f-4e88-a9b7-294c41143402, mf.imfqualityadvise_getdropmode, mfidl/IMFQualityAdvise::GetDropMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFQualityAdvise.GetDropMode
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityAdvise::GetDropMode


## -description



Retrieves the current drop mode.




## -parameters




### -param peDropMode [out]

Receives the drop mode, specified as a member of the <a href="https://msdn.microsoft.com/e40751d2-9abf-4fe6-8829-9b1fbf4531e8">MF_QUALITY_DROP_MODE</a> enumeration.


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




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>
 

 

