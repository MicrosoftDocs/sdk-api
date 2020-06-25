---
UID: NN:imapi2.IDiscRecorder2
title: IDiscRecorder2 (imapi2.h)
description: This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.
helpviewer_keywords: ["IDiscRecorder2","IDiscRecorder2 interface [IMAPI]","IDiscRecorder2 interface [IMAPI]","described","imapi.idiscrecorder2","imapi2/IDiscRecorder2"]
old-location: imapi\idiscrecorder2.htm
tech.root: imapi
ms.assetid: 34f858b8-74eb-4725-8815-7954cb98cff0
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2, IDiscRecorder2 interface [IMAPI], IDiscRecorder2 interface [IMAPI],described, imapi.idiscrecorder2, imapi2/IDiscRecorder2
f1_keywords:
- imapi2/IDiscRecorder2
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
- IDiscRecorder2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscRecorder2 interface


## -description


This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscRecorder2) for the class identifier and __uuidof(IDiscRecorder2) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscRecorder2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscRecorder2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-acquireexclusiveaccess">AcquireExclusiveAccess</a>
</td>
<td align="left" width="63%">
Acquires exclusive access to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-closetray">CloseTray</a>
</td>
<td align="left" width="63%">
Closes the media tray.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-disablemcn">DisableMcn</a>
</td>
<td align="left" width="63%">
Disables Media Change Notification for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-ejectmedia">EjectMedia</a>
</td>
<td align="left" width="63%">
Ejects media from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-enablemcn">EnableMcn</a>
</td>
<td align="left" width="63%">
Enables Media Change Notification for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_activediscrecorder">get_ActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier used to initialize the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_currentfeaturepages">get_CurrentFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of features of the device that are marked as current.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_currentprofiles">get_CurrentProfiles</a>
</td>
<td align="left" width="63%">
Retrieves all MMC profiles of the device that are marked as current.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_devicecanloadmedia">get_DeviceCanLoadMedia</a>
</td>
<td align="left" width="63%">
Determines if the device can eject and subsequently reload media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_exclusiveaccessowner">get_ExclusiveAccessOwner</a>
</td>
<td align="left" width="63%">
Retrieves the name of the user that has exclusive access to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_legacydevicenumber">get_LegacyDeviceNumber</a>
</td>
<td align="left" width="63%">
Retrieves  the legacy device number for a CD or DVD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_productid">get_ProductId</a>
</td>
<td align="left" width="63%">
Retrieves the product ID of  the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_productrevision">get_ProductRevision</a>
</td>
<td align="left" width="63%">
Retrieves the product revision code of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_supportedfeaturepages">get_SupportedFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of features that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_supportedmodepages">get_SupportedModePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of MMC mode pages that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_supportedprofiles">get_SupportedProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the list of MMC profiles that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_vendorid">get_VendorId</a>
</td>
<td align="left" width="63%">
Retrieves the vendor ID of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_volumename">get_VolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the unique volume name associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_volumepathnames">get_VolumePathNames</a>
</td>
<td align="left" width="63%">
Retrieves the drive letters and NTFS mount points for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-initializediscrecorder">InitializeDiscRecorder</a>
</td>
<td align="left" width="63%">
Associates the object with the specified disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-releaseexclusiveaccess">ReleaseExclusiveAccess</a>
</td>
<td align="left" width="63%">
Releases exclusive access to the device.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscRecorder2</b> object in a script, use IMAPI2.MsftDiscRecorder2 as the program identifier when calling <b>CreateObject</b>.

To write data to media, you need to attach a recorder to a format writer, for example, to attach the recorder to a data writer, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder">IDiscFormat2Data::put_Recorder</a> method.

Several properties of this interface return packet data defined by Multimedia Command (MMC). For information on the format of the packet data, see the latest revision of the MMC specification at ftp://ftp.t10.org/t10/drafts/mmc5.  




## -see-also




IDiscRecorder2Ex
 

 

