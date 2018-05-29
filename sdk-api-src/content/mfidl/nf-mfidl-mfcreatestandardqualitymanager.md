---
UID: NF:mfidl.MFCreateStandardQualityManager
title: MFCreateStandardQualityManager function
author: windows-sdk-content
description: Creates the default implementation of the quality manager.
old-location: mf\mfcreatestandardqualitymanager.htm
old-project: medfound
ms.assetid: 9abaa474-8a00-4e36-897d-9de9578333b7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9abaa474-8a00-4e36-897d-9de9578333b7, MFCreateStandardQualityManager, MFCreateStandardQualityManager function [Media Foundation], mf.mfcreatestandardqualitymanager, mfidl/MFCreateStandardQualityManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateStandardQualityManager
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateStandardQualityManager function


## -description



Creates the default implementation of the quality manager.




## -parameters




### -param ppQualityManager [out]

Receives a pointer to the quality manager's <a href="https://msdn.microsoft.com/66781a1f-7469-4222-9e99-6b1415830f4c">IMFQualityManager</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

