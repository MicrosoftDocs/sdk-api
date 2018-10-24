---
UID: NN:imapi2.IDiscRecorder2Ex
title: IDiscRecorder2Ex
author: windows-sdk-content
description: This interface represents a physical device.
old-location: imapi\idiscrecorder2ex.htm
tech.root: imapi
ms.assetid: 37e65b57-ec53-405c-a7bd-34c2df15d5d7
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDiscRecorder2Ex, IDiscRecorder2Ex interface [IMAPI], IDiscRecorder2Ex interface [IMAPI],described, imapi.idiscrecorder2ex, imapi2/IDiscRecorder2Ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder2Ex interface


## -description


This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or ejecting the media. This interface retrieves information not available through <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface, and provides easier access to some of the same property values in <b>IDiscRecorder2</b>.

To get an instance of this interface, create an instance of the <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface and then call the <b>IDiscRecorder2::QueryInterface</b> method to retrieve the <b>IDiscRecorder2Ex</b> interface.

Note that you cannot access this functionality from script.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder2Ex</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IDiscRecorder2Ex</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3922243c-97cf-43e3-a437-a5157ed73559">GetAdapterDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the adapter descriptor for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a92efb1-4da8-4cf4-8011-b06a0f82a3eb">GetByteAlignmentMask</a>
</td>
<td align="left" width="63%">
Retrieves the byte alignment mask for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0c22ce6-daf4-4218-afce-c773d607638b">GetDeviceDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the device descriptor for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f2888cb-3f9e-4dc3-ba9a-c13a0a46f731">GetDiscInformation</a>
</td>
<td align="left" width="63%">
Retrieves the disc information from the media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3cf0d33-25ea-4764-8fdb-5ef47c7b1e50">GetFeaturePage</a>
</td>
<td align="left" width="63%">
Retrieves the specified feature page from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dae56eb7-8fd5-40ea-b3de-2f98206a5cb2">GetMaximumNonPageAlignedTransferSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum non-page-aligned transfer size for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bf25c61-e87c-4ccf-a989-1c2715709d4a">GetMaximumPageAlignedTransferSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum page-aligned transfer size for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69e163a6-943d-4626-8120-778c9ca1777f">GetModePage</a>
</td>
<td align="left" width="63%">
Retrieves the specified mode page from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64fa8ef5-1298-4fd1-b89d-371f13e50d8c">GetSupportedFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of supported feature pages or the current feature pages of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/343d976e-97f3-4231-a417-4ebe7967f99c">GetSupportedModePages</a>
</td>
<td align="left" width="63%">
Retrieves the supported mode pages for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1295d536-8531-4470-a8b4-1e589736e0b1">GetSupportedProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the supported profiles or the current profiles of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfb8c7b0-8fe4-4e41-8e71-31ea0af57619">GetTrackInformation</a>
</td>
<td align="left" width="63%">
Retrieves the track  information from the media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6842573a-68e5-47ea-8441-953ab85b9482">ReadDvdStructure</a>
</td>
<td align="left" width="63%">
Reads a DVD structure from the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3142b79-4e46-4cb8-ab4a-3bf5823cd26e">SendCommandGetDataFromDevice</a>
</td>
<td align="left" width="63%">
Sends a MMC command to the recording device requesting data from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dc645d5-795d-4f31-a4cf-30875e930e10">SendCommandNoData</a>
</td>
<td align="left" width="63%">
Sends a MMC command to the recording device. Use this function when no data buffer is sent to nor received from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e893c3d8-1bf8-461e-9792-3b7d6d3beebb">SendCommandSendDataToDevice</a>
</td>
<td align="left" width="63%">
Sends a MMC command and its associated data buffer to the recording device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e9b83ee-69f6-42b8-bd6b-546c4ffe2002">SendDvdStructure</a>
</td>
<td align="left" width="63%">
Sends a DVD structure to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ca1e8c0-d75d-40a7-8b2e-5c240c410031">SetModePage</a>
</td>
<td align="left" width="63%">
Sets the mode page data for the device.

</td>
</tr>
</table> 


## -remarks



To write data to media, you need to attach this recorder to the <a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a> data writer, using the <a href="https://msdn.microsoft.com/3ab46d99-7940-4ad0-9772-634de8c0d0ef">IWriteEngine2::put_Recorder</a> method.




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>
 

 

