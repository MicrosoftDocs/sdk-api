---
UID: NN:imapi2.IDiscRecorder2
title: IDiscRecorder2
author: windows-sdk-content
description: This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.
old-location: imapi\idiscrecorder2.htm
tech.root: imapi
ms.assetid: 34f858b8-74eb-4725-8815-7954cb98cff0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDiscRecorder2, IDiscRecorder2 interface [IMAPI], IDiscRecorder2 interface [IMAPI],described, imapi.idiscrecorder2, imapi2/IDiscRecorder2
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
 - IDiscRecorder2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder2 interface


## -description


This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscRecorder2) for the class identifier and __uuidof(IDiscRecorder2) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IDiscRecorder2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/58cb5efa-74bc-4444-aa05-be41a6c63b3a">AcquireExclusiveAccess</a>
</td>
<td align="left" width="63%">
Acquires exclusive access to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a30f3bb-68fc-45d5-826d-79ed9209f391">CloseTray</a>
</td>
<td align="left" width="63%">
Closes the media tray.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3111863e-64bf-467c-ac73-7a16c9aeb3df">DisableMcn</a>
</td>
<td align="left" width="63%">
Disables Media Change Notification for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8fc55d7-0840-4090-a653-eb38d3f37fac">EjectMedia</a>
</td>
<td align="left" width="63%">
Ejects media from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce848ba1-86b4-44cc-8f41-8b8eaba20521">EnableMcn</a>
</td>
<td align="left" width="63%">
Enables Media Change Notification for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fd3e13c-2853-417e-8478-46fa667c9f97">get_ActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier used to initialize the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27504cb3-5c78-4fcb-8d37-ce7e6ac2a006">get_CurrentFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of features of the device that are marked as current.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd8dd2fd-531b-4ed5-9a28-d6b24469e5e7">get_CurrentProfiles</a>
</td>
<td align="left" width="63%">
Retrieves all MMC profiles of the device that are marked as current.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa6790aa-2999-4895-83fa-3967cb411741">get_DeviceCanLoadMedia</a>
</td>
<td align="left" width="63%">
Determines if the device can eject and subsequently reload media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32577b35-235a-4186-8fb3-18e5555cb56f">get_ExclusiveAccessOwner</a>
</td>
<td align="left" width="63%">
Retrieves the name of the user that has exclusive access to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14ec2007-3648-49b6-a96e-b682d592c2f1">get_LegacyDeviceNumber</a>
</td>
<td align="left" width="63%">
Retrieves  the legacy device number for a CD or DVD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f0bfdd4-059f-40c0-9da1-fa842bd415de">get_ProductId</a>
</td>
<td align="left" width="63%">
Retrieves the product ID of  the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d727937-8581-4001-96f2-f83795e1ee52">get_ProductRevision</a>
</td>
<td align="left" width="63%">
Retrieves the product revision code of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2764de1-85cc-4f04-951d-5cb70575ee9f">get_SupportedFeaturePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of features that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a6fe1c3-7ce2-4877-93e6-de4ab87685a0">get_SupportedModePages</a>
</td>
<td align="left" width="63%">
Retrieves the list of MMC mode pages that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ee1b58b-0289-42e8-a23d-2600b9dd2e21">get_SupportedProfiles</a>
</td>
<td align="left" width="63%">
Retrieves the list of MMC profiles that the device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3e76907-1960-4c13-b6e4-9f5c86de38c6">get_VendorId</a>
</td>
<td align="left" width="63%">
Retrieves the vendor ID of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/953f291d-a1b8-4cad-8ddf-59e251de65f2">get_VolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the unique volume name associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e07553f-0d90-4b7d-95f8-0fe02c348695">get_VolumePathNames</a>
</td>
<td align="left" width="63%">
Retrieves the drive letters and NTFS mount points for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19a647b3-ef39-4208-9dfc-e52242a88c6c">InitializeDiscRecorder</a>
</td>
<td align="left" width="63%">
Associates the object with the specified disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/940929d7-7940-448e-9554-3e3691772eb8">ReleaseExclusiveAccess</a>
</td>
<td align="left" width="63%">
Releases exclusive access to the device.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscRecorder2</b> object in a script, use IMAPI2.MsftDiscRecorder2 as the program identifier when calling <b>CreateObject</b>.

To write data to media, you need to attach a recorder to a format writer, for example, to attach the recorder to a data writer, call the <a href="https://msdn.microsoft.com/d8d1f6ec-09cb-4144-b44c-970555451aee">IDiscFormat2Data::put_Recorder</a> method.

Several properties of this interface return packet data defined by Multimedia Command (MMC). For information on the format of the packet data, see the latest revision of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.  




## -see-also




IDiscRecorder2Ex
 

 

