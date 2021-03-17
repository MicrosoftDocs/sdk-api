---
UID: NF:mfidl.IMFSensorActivitiesReport.GetCount
title: IMFSensorActivitiesReport::GetCount (mfidl.h)
description: Gets the count of IMFSensorActivityReport objects that are available to be retrieved.
helpviewer_keywords: ["GetCount","GetCount method [Media Foundation]","GetCount method [Media Foundation]","IMFSensorActivitiesReport interface","IMFSensorActivitiesReport interface [Media Foundation]","GetCount method","IMFSensorActivitiesReport.GetCount","IMFSensorActivitiesReport::GetCount","mf.imfsensoractivityreport_getcount","mfidl/IMFSensorActivitiesReport::GetCount"]
old-location: mf\imfsensoractivityreport_getcount.htm
tech.root: mf
ms.assetid: 459A0898-ED5F-479F-8DDC-EA67C04F7BF9
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Media Foundation], GetCount method [Media Foundation],IMFSensorActivitiesReport interface, IMFSensorActivitiesReport interface [Media Foundation],GetCount method, IMFSensorActivitiesReport.GetCount, IMFSensorActivitiesReport::GetCount, mf.imfsensoractivityreport_getcount, mfidl/IMFSensorActivitiesReport::GetCount
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorActivitiesReport::GetCount
 - mfidl/IMFSensorActivitiesReport::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorActivitiesReport.GetCount
---

# IMFSensorActivitiesReport::GetCount


## -description

Gets the count of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> objects that are available to be retrieved.

## -parameters

### -param pcCount [out]

The count of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> objects that are available to be retrieved.

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
The <i>pcCount</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>