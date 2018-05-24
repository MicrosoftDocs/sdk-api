---
UID: NF:mswmdm.IMDSPDeviceControl.Seek
title: IMDSPDeviceControl::Seek
author: windows-driver-content
description: The Seek method seeks to a position that is used as the starting point by the Play or Record methods.
old-location: wmdm\imdspdevicecontrol_seek.htm
old-project: WMDM
ms.assetid: 05fbaab8-e1fa-4960-9591-d22347bc04f2
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Seek method, IMDSPDeviceControl.Seek, IMDSPDeviceControl::Seek, IMDSPDeviceControlSeek, Seek, Seek method [windows Media Device Manager], Seek method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Seek, wmdm.imdspdevicecontrol_seek
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IMDSPDeviceControl.Seek
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDeviceControl::Seek


## -description



The <b>Seek</b> method seeks to a position that is used as the starting point by the <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">Play</a> or <a href="https://msdn.microsoft.com/6cd99cfc-1961-4369-9ce9-2cdd0136d181">Record</a> methods.




## -parameters




### -param fuMode [in]

Mode for the seek operation being performed. The <i>fuMode</i> parameter must be one of the following modes.

<table>
<tr>
<th>
                  Mode
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MDSP_SEEK_BOF</td>
<td>Seek to a position that is <i>nOffset</i> units after the beginning of the file.</td>
</tr>
<tr>
<td>MDSP_SEEK_CUR</td>
<td>Seek to a position that is <i>nOffset</i> units from the current position.</td>
</tr>
<tr>
<td>MDSP_SEEK_EOF</td>
<td>Seek to a position that is <i>nOffset</i> units before the end of the file.</td>
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



The seek position is defined by passing either an <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface pointing to a location on a storage medium of the device, or an <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a> interface that has been implemented to support streaming audio. The <a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo</a> interface can also be passed to describe some point within the object to which the specified interface points.

For device playback, if <b>Seek</b> is not called before <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">Play</a>, then playback starts at the first audio track on the first storage medium on the media device.

For device recording, if <b>Seek</b> is not called before <a href="https://msdn.microsoft.com/6cd99cfc-1961-4369-9ce9-2cdd0136d181">Record</a>, the record operation fails. After the <b>Record</b> method is called, subsequent calls to the <a href="https://msdn.microsoft.com/7ebd73b2-d168-470b-bc5a-aad8888c401a">IMDSPObjectInfo::GetLastPlayPosition</a> method report the total play length at any time, and equal the value returned from <a href="https://msdn.microsoft.com/abd18861-550b-4968-ac96-05f07315d4db">IMDSPObjectInfo::GetTotalLength</a>. The recording length can be limited by calling the <a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">IMDSPObjectInfo::SetPlayLength</a> method after returning from the <b>Seek</b> call.




## -see-also




<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

