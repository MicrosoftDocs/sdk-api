---
UID: NN:imapi2.IDiscRecorder2Ex
title: IDiscRecorder2Ex (imapi2.h)
description: This interface represents a physical device.
old-location: imapi\idiscrecorder2ex.htm
tech.root: imapi
ms.assetid: 37e65b57-ec53-405c-a7bd-34c2df15d5d7
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2Ex, IDiscRecorder2Ex interface [IMAPI], IDiscRecorder2Ex interface [IMAPI],described, imapi.idiscrecorder2ex, imapi2/IDiscRecorder2Ex
f1_keywords:
- imapi2/IDiscRecorder2Ex
dev_langs:
- c++
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
- imapi2.h
api_name:
- IDiscRecorder2Ex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscRecorder2Ex interface


## -description


This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or ejecting the media. This interface retrieves information not available through <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface, and provides easier access to some of the same property values in <b>IDiscRecorder2</b>.

To get an instance of this interface, create an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface and then call the <b>IDiscRecorder2::QueryInterface</b> method to retrieve the <b>IDiscRecorder2Ex</b> interface.

Note that you cannot access this functionality from script.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder2Ex</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscRecorder2Ex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscRecorder2Ex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getadapterdescriptor">GetAdapterDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the adapter descriptor for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getbytealignmentmask">GetByteAlignmentMask</a>
</td>
<td align="left" width="63%">
Retrieves the byte alignment mask for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getdevicedescriptor">GetDeviceDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the device descriptor for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getdiscinformation">GetDiscInformation</a>
</td>
<td align="left" width="63%">
Retrieves the disc information from the media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getfeaturepage">GetFeaturePage</a>
</td>
<td align="left" width="63%">
Retrieves the specified feature page from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmaximumnonpagealignedtransfersize">GetMaximumNonPageAlignedTransferSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum non-page-aligned transfer size for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmaximumpagealignedtransfersize">GetMaximumPageAlignedTransferSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum page-aligned transfer size for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmodepage">GetModePage</a>
</td>
<td align="left" width="63%">
Retrieves the specified mode page from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getsupportedfeaturepages">GetSupportedFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of supported feature pages or the current feature pages of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getsupportedmodepages">GetSupportedModePages</a>
</td>
<td align="left" width="63%">
Retrieves the supported mode pages for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getsupportedprofiles">GetSupportedProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the supported profiles or the current profiles of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-gettrackinformation">GetTrackInformation</a>
</td>
<td align="left" width="63%">
Retrieves the track  information from the media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-readdvdstructure">ReadDvdStructure</a>
</td>
<td align="left" width="63%">
Reads a DVD structure from the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandgetdatafromdevice">SendCommandGetDataFromDevice</a>
</td>
<td align="left" width="63%">
Sends a MMC command to the recording device requesting data from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandnodata">SendCommandNoData</a>
</td>
<td align="left" width="63%">
Sends a MMC command to the recording device. Use this function when no data buffer is sent to nor received from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandsenddatatodevice">SendCommandSendDataToDevice</a>
</td>
<td align="left" width="63%">
Sends a MMC command and its associated data buffer to the recording device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-senddvdstructure">SendDvdStructure</a>
</td>
<td align="left" width="63%">
Sends a DVD structure to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-setmodepage">SetModePage</a>
</td>
<td align="left" width="63%">
Sets the mode page data for the device.

</td>
</tr>
</table> 


## -remarks



To write data to media, you need to attach this recorder to the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a> data writer, using the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_recorder">IWriteEngine2::put_Recorder</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>
 

 

