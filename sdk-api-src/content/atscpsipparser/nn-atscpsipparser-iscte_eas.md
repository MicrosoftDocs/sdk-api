---
UID: NN:atscpsipparser.ISCTE_EAS
title: ISCTE_EAS (atscpsipparser.h)
description: The ISCTE_EAS interface enables the client to get data from an ATSC emergency alert message (EAS) table.
helpviewer_keywords: ["ISCTE_EAS","ISCTE_EAS interface [Microsoft TV Technologies]","ISCTE_EAS interface [Microsoft TV Technologies]","described","ISCTE_EASInterface","atscpsipparser/ISCTE_EAS","mstv.iscte_eas"]
old-location: mstv\iscte_eas.htm
tech.root: mstv
ms.assetid: 7b5620c3-f460-4118-a8a2-9b2561bd12cf
ms.date: 12/05/2018
ms.keywords: ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], ISCTE_EAS interface [Microsoft TV Technologies],described, ISCTE_EASInterface, atscpsipparser/ISCTE_EAS, mstv.iscte_eas
f1_keywords:
- atscpsipparser/ISCTE_EAS
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- atscpsipparser.h
api_name:
- ISCTE_EAS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS interface


## -description


The <b>ISCTE_EAS</b> interface enables the client to get data from an ATSC emergency alert message (EAS) table. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteas">IAtscPsipParser::GetEAS</a> method returns a pointer to this interface.

For more information about EAS tables, see ANSI-J-STD-042-A, Emergency Alert Message for Cable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCTE_EAS</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCTE_EAS</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getalertpriority">GetAlertPriority</a>
</td>
<td align="left" width="63%">
Returns the alert priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getalerttext">GetAlertText</a>
</td>
<td align="left" width="63%">
gets the alert text for a specified ISO 639 language code

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getdetailsaudiooobsourceid">GetDetailsAudioOOBSourceID</a>
</td>
<td align="left" width="63%">
Returns the source identifier of the virtual audio channel for the emergency alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getdetailsmajor">GetDetailsMajor</a>
</td>
<td align="left" width="63%">
Returns the major channel number for the details channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getdetailsminor">GetDetailsMinor</a>
</td>
<td align="left" width="63%">
Returns the minor channel number for the details channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getdetailsoobsourceid">GetDetailsOOBSourceID</a>
</td>
<td align="left" width="63%">
Returns the source identifier of the virtual details channel for the emergency alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Returns the expected duration of the alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventcode">GetEASEventCode</a>
</td>
<td align="left" width="63%">
Returns the EAS event code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventcodelen">GetEASEventCodeLen</a>
</td>
<td align="left" width="63%">
Returns the size of the EAS event code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventid">GetEASEventID</a>
</td>
<td align="left" width="63%">
Returns the identifier of this emergency event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getexceptioncount">GetExceptionCount</a>
</td>
<td align="left" width="63%">
Returns the number of exception services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getexceptionservice">GetExceptionService</a>
</td>
<td align="left" width="63%">
Returns information about an exception service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getlocationcodes">GetLocationCodes</a>
</td>
<td align="left" width="63%">
Returns location codes from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getlocationcount">GetLocationCount</a>
</td>
<td align="left" width="63%">
Returns the number of locations in the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getnatureofactivationtext">GetNatureOfActivationText</a>
</td>
<td align="left" width="63%">
Gets a textual representation of the alert for a specified ISO 639 language code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getoriginatorcode">GetOriginatorCode</a>
</td>
<td align="left" width="63%">
Returns the EAS originator code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getprotocolversion">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawalerttext">GetRawAlertText</a>
</td>
<td align="left" width="63%">
Gets the raw alert_text field from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawalerttextlen">GetRawAlertTextLen</a>
</td>
<td align="left" width="63%">
Gets the length of the alert_text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawnatureofactivationtext">GetRawNatureOfActivationText</a>
</td>
<td align="left" width="63%">
Gets the raw nature_of_activation_text field from the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawnatureofactivationtextlen">GetRawNatureOfActivationTextLen</a>
</td>
<td align="left" width="63%">
Gets the length of the nature_of_activation_text field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getsequencynumber">GetSequencyNumber</a>
</td>
<td align="left" width="63%">
Returns the sequence number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getstarttime">GetStartTime</a>
</td>
<td align="left" width="63%">
Returns the starting time of the alert.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-gettabledescriptorbyindex">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the EAS table for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-gettimeremaining">GetTimeRemaining</a>
</td>
<td align="left" width="63%">
Returns the time that remains in the alert message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the EAS table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

