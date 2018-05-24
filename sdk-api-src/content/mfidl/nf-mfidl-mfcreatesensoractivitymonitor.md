---
UID: NF:mfidl.MFCreateSensorActivityMonitor
title: MFCreateSensorActivityMonitor function
author: windows-driver-content
description: Initializes a new instance of the IMFSensorActivityMonitor interface.
old-location: mf\mfcreatesensoractivitymonitor.htm
old-project: medfound
ms.assetid: 852395EE-AA84-4C61-A55F-E8D925FA1447
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: MFCreateSensorActivityMonitor, MFCreateSensorActivityMonitor function [Media Foundation], mf.mfcreatesensoractivitymonitor, mfidl/MFCreateSensorActivityMonitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	mfsensorgroup.lib
api_name:
-	MFCreateSensorActivityMonitor
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.lib
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateSensorActivityMonitor function


## -description


Initializes a new instance of the <a href="https://msdn.microsoft.com/1D0F8C4E-CB64-4787-A25F-8D826356226C">IMFSensorActivityMonitor</a> interface.


## -parameters




### -param pCallback [in]

An implementation of the <a href="https://msdn.microsoft.com/477B008D-7F0A-4084-BDFD-DF19E2A82817">IMFSensorActivitiesReportCallback</a> interface through which the system delivers <a href="https://msdn.microsoft.com/CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3">IMFSensorActivitiesReport</a> objects.


### -param ppActivityMonitor [out]

A pointer to the new <a href="https://msdn.microsoft.com/1D0F8C4E-CB64-4787-A25F-8D826356226C">IMFSensorActivityMonitor</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppActivityMonitor</i> parameter is null.

</td>
</tr>
</table>
 



