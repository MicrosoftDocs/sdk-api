---
UID: NF:mfidl.MFCreateSensorActivityMonitor
title: MFCreateSensorActivityMonitor function (mfidl.h)
description: Initializes a new instance of the IMFSensorActivityMonitor interface.
helpviewer_keywords: ["MFCreateSensorActivityMonitor","MFCreateSensorActivityMonitor function [Media Foundation]","mf.mfcreatesensoractivitymonitor","mfidl/MFCreateSensorActivityMonitor"]
old-location: mf\mfcreatesensoractivitymonitor.htm
tech.root: mf
ms.assetid: 852395EE-AA84-4C61-A55F-E8D925FA1447
ms.date: 12/05/2018
ms.keywords: MFCreateSensorActivityMonitor, MFCreateSensorActivityMonitor function [Media Foundation], mf.mfcreatesensoractivitymonitor, mfidl/MFCreateSensorActivityMonitor
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
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.lib
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSensorActivityMonitor
 - mfidl/MFCreateSensorActivityMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfsensorgroup.lib
 - mfplat.dll
api_name:
 - MFCreateSensorActivityMonitor
---

# MFCreateSensorActivityMonitor function


## -description

Initializes a new instance of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor">IMFSensorActivityMonitor</a> interface.

## -parameters

### -param pCallback [in]

An implementation of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a> interface through which the system delivers <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a> objects.

### -param ppActivityMonitor [out]

A pointer to the new <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor">IMFSensorActivityMonitor</a>.

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