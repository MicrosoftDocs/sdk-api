---
UID: NN:atscpsipparser.ISCTE_EAS
title: ISCTE_EAS
author: windows-driver-content
description: The ISCTE_EAS interface enables the client to get data from an ATSC emergency alert message (EAS) table.
old-location: mstv\iscte_eas.htm
old-project: mstv
ms.assetid: 7b5620c3-f460-4118-a8a2-9b2561bd12cf
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], ISCTE_EAS interface [Microsoft TV Technologies],described, ISCTE_EASInterface, atscpsipparser/ISCTE_EAS, mstv.iscte_eas
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS interface


## -description


The <b>ISCTE_EAS</b> interface enables the client to get data from an ATSC emergency alert message (EAS) table. The <a href="https://msdn.microsoft.com/e53b93e3-7269-45aa-8b19-75f78fb44c41">IAtscPsipParser::GetEAS</a> method returns a pointer to this interface.

For more information about EAS tables, see ANSI-J-STD-042-A, Emergency Alert Message for Cable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCTE_EAS</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISCTE_EAS</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCTE_EAS</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3862ae19-972b-4822-8b52-5a868a2fc58d">GetAlertPriority</a>
</td>
<td align="left" width="63%">
Returns the alert priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bef1a14-b0f6-40a0-bac0-1d6c00c120e5">GetAlertText</a>
</td>
<td align="left" width="63%">
gets the alert text for a specified ISO 639 language code

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d6cae55-233f-49e0-8ced-9dd21b0aa32b">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab054225-e8e6-4f78-9010-15fc8e5ad15b">GetDetailsAudioOOBSourceID</a>
</td>
<td align="left" width="63%">
Returns the source identifier of the virtual audio channel for the emergency alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb6f06d-ccf5-44f3-ba36-b24176c3a20e">GetDetailsMajor</a>
</td>
<td align="left" width="63%">
Returns the major channel number for the details channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59d43d84-2120-4200-b1e7-4603c1693018">GetDetailsMinor</a>
</td>
<td align="left" width="63%">
Returns the minor channel number for the details channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50bf2acd-87e1-4b64-bf98-997603d56a0a">GetDetailsOOBSourceID</a>
</td>
<td align="left" width="63%">
Returns the source identifier of the virtual details channel for the emergency alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de644588-6247-44d2-9d19-53272af8529b">GetDuration</a>
</td>
<td align="left" width="63%">
Returns the expected duration of the alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9618fb6f-61f3-44cf-9605-b47a6a1e9be6">GetEASEventCode</a>
</td>
<td align="left" width="63%">
Returns the EAS event code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6e05cd0-d043-4f15-b25b-28402035943b">GetEASEventCodeLen</a>
</td>
<td align="left" width="63%">
Returns the size of the EAS event code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d501fa7c-c1a8-42bc-af71-a966a7cba9f6">GetEASEventID</a>
</td>
<td align="left" width="63%">
Returns the identifier of this emergency event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da98cf2f-a302-41d0-8226-18d6bb89be82">GetExceptionCount</a>
</td>
<td align="left" width="63%">
Returns the number of exception services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9431651-4f8f-40a0-abd8-b162e5ad09ae">GetExceptionService</a>
</td>
<td align="left" width="63%">
Returns information about an exception service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31fa68d4-1719-4a93-bec9-6a7ba4f36c0b">GetLocationCodes</a>
</td>
<td align="left" width="63%">
Returns location codes from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f498ead0-246d-4741-a995-45a5cf63847e">GetLocationCount</a>
</td>
<td align="left" width="63%">
Returns the number of locations in the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">GetNatureOfActivationText</a>
</td>
<td align="left" width="63%">
Gets a textual representation of the alert for a specified ISO 639 language code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a46f0922-9733-411a-8a03-59e1c98dbdd8">GetOriginatorCode</a>
</td>
<td align="left" width="63%">
Returns the EAS originator code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80700a74-85d6-4269-9000-83e62f68aeb1">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5ed18e8-e83e-4708-995b-99acd12427a7">GetRawAlertText</a>
</td>
<td align="left" width="63%">
Gets the raw alert_text field from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e85b1deb-6e93-4187-8a18-80740ce9e4c9">GetRawAlertTextLen</a>
</td>
<td align="left" width="63%">
Gets the length of the alert_text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11ada9ab-b55f-41c1-9d7d-1c856a17a3a9">GetRawNatureOfActivationText</a>
</td>
<td align="left" width="63%">
Gets the raw nature_of_activation_text field from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7f93884-d8a9-449b-afc2-b2ccbd0d2492">GetRawNatureOfActivationTextLen</a>
</td>
<td align="left" width="63%">
Gets the length of the nature_of_activation_text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7988bb1-0c89-4f6f-beda-cbfd04a9b128">GetSequencyNumber</a>
</td>
<td align="left" width="63%">
Returns the sequence number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70847a50-67a1-49f1-a24f-ca5bb0309481">GetStartTime</a>
</td>
<td align="left" width="63%">
Returns the starting time of the alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24e02875-32ab-4844-bec3-8044b03b9843">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91e0aad8-31d9-44d1-9bda-7f0134f5457b">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the EAS table for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d04408f-a1ff-41cf-8ab0-1f30e700b07b">GetTimeRemaining</a>
</td>
<td align="left" width="63%">
Returns the time that remains in the alert message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2108435-37ef-404c-b735-a5100acfa8a4">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

