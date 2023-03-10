---
UID: NF:mswmdm.IWMDMDeviceControl.Seek
title: IWMDMDeviceControl::Seek (mswmdm.h)
description: The Seek method seeks to a position that is used as the starting point by the Play or Record methods. (IWMDMDeviceControl.Seek)
helpviewer_keywords: ["IWMDMDeviceControl interface [windows Media Device Manager]","Seek method","IWMDMDeviceControl.Seek","IWMDMDeviceControl::Seek","IWMDMDeviceControlSeek","Seek","Seek method [windows Media Device Manager]","Seek method [windows Media Device Manager]","IWMDMDeviceControl interface","mswmdm/IWMDMDeviceControl::Seek","wmdm.iwmdmdevicecontrol_seek"]
old-location: wmdm\iwmdmdevicecontrol_seek.htm
tech.root: WMDM
ms.assetid: f416a520-197c-4607-979e-8f43951f2076
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Seek method, IWMDMDeviceControl.Seek, IWMDMDeviceControl::Seek, IWMDMDeviceControlSeek, Seek, Seek method [windows Media Device Manager], Seek method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Seek, wmdm.iwmdmdevicecontrol_seek
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDeviceControl::Seek
 - mswmdm/IWMDMDeviceControl::Seek
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDeviceControl.Seek
---

# IWMDMDeviceControl::Seek


## -description

The <b>Seek</b> method seeks to a position that is used as the starting point by the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-record">Record</a> methods.

## -parameters

### -param fuMode [in]

Mode for the seek operation being performed. The <i>fuMode</i> parameter must be one of the following modes.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SEEK_BEGIN</td>
<td>Seek to a position that is <i>nOffset</i> units after the beginning of the file.</td>
</tr>
<tr>
<td>WMDM_SEEK_CURRENT</td>
<td>Seek to a position that is <i>nOffset</i> units from the current position.</td>
</tr>
<tr>
<td>WMDM_SEEK_END</td>
<td>Seek to a position that is <i>nOffset</i> units before the end of the file.</td>
</tr>
<tr>
<td>WMDM_SEEK_REMOTECONTROL</td>
<td>Seek the removable control.</td>
</tr>
<tr>
<td>WMDM_SEEK_STREAMINGAUDIO</td>
<td>Seek the streaming audio.</td>
</tr>
</table>

### -param nOffset [in]

Number of units by which the seek operation moves the starting position away from the origin specified by <i>fuMode</i>. The units of <i>nOffset</i> are defined by the content. They can be milliseconds for music, pages for electronic books, and so on.

A positive value for <i>nOffset</i> indicates seeking forward through the file. A negative value indicates seeking backward through the file. Any combination of <i>nOffset</i> and <i>fuMode</i> that indicates seeking to a position before the beginning of the file or after the end of the file is not valid, and causes the method to return E_INVALIDARG.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Seek is not implemented on this device.

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
</table>

## -remarks

The seek position is defined by passing either an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a> interface pointing to a location on a storage medium of the device, or an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation</a> interface that has been implemented to support streaming audio. The <b>IWMDMObjectInfo</b> interface can also be passed to describe some point within the object to which the specified interface points.

For device playback, if <b>Seek</b> is not called before <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a>, then playback starts at the first audio track on the first storage medium on the media device.

For device recording, if <b>Seek</b> is not called before <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-record">Record</a>, the record operation fails. The recording length can be limited by calling the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplaylength">IWMDMObjectInfo::SetPlayLength</a> method after returning from the <b>Seek</b> call.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>
