---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ADDRESS_CAPABILITY enumeration


## -description


A member of the 
<b>ADDRESS_CAPABILITY</b> enum is used by the 
<a href="https://msdn.microsoft.com/76e61d5e-48b6-4b9c-9076-bd20a794859c">ITAddressCapabilities::get_AddressCapability</a> method to indicate the address capability required.


## -enum-fields




### -field AC_ADDRESSTYPES

An address may support more than one 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a>, but please note that one may be used during 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>.


### -field AC_BEARERMODES


<a href="https://msdn.microsoft.com/87e46ec9-ed5f-4ff5-a382-34eb164f4e66">Bearer modes</a>.


### -field AC_MAXACTIVECALLS

The maximum number of (minimum bandwidth) calls that can be active (connected) on the line at any one time. The actual number of active calls can be lower if higher bandwidth calls are established on the line.


### -field AC_MAXONHOLDCALLS

Maximum number of calls that can be on hold at once.


### -field AC_MAXONHOLDPENDINGCALLS

Maximum number of calls that can be simultaneously pending transfer or conference.


### -field AC_MAXNUMCONFERENCE

Contains the maximum number of parties that can join a single conference call on this address.


### -field AC_MAXNUMTRANSCONF

Specifies the number of parties (including "self") that can be added in a conference call that is initiated as a generic consultation call using 
<a href="https://msdn.microsoft.com/4f2a06e6-9f0b-4bf3-9f18-6e9f57c4b02f">ITBasicCallControl::Transfer</a> and 
<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">ITBasicCallControl::Finish</a> (FM_ASCONFERENCE).


### -field AC_MONITORDIGITSUPPORT

Specifies digit modes detectable on this address using the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_</a> flags. If no flag is set, digit monitoring is not supported.


### -field AC_GENERATEDIGITSUPPORT

Specifies digit modes that can be generated on this address using a subset of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_</a> flags: LINEDIGITMODE_PULSE indicates digits can be generated as pulse/rotary tones, and LINEDIGITMODE_DTMF indicates digits can be generated as DTMF tones. If no flag is set, digit generation is not supported.


### -field AC_GENERATETONEMODES

Specifies the different kinds of tones that can be generated on this line, of type 
<a href="https://msdn.microsoft.com/7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263">LINETONEMODE_</a>.


### -field AC_GENERATETONEMAXNUMFREQ

Contains the maximum number of frequencies that can be specified in describing a general tone.


### -field AC_MONITORTONEMAXNUMFREQ

Contains the maximum number of frequencies that can be specified when monitoring a general tone. A value of 0 indicates that tone monitor is not available.


### -field AC_MONITORTONEMAXNUMENTRIES

Contains the maximum number of entries that can be specified in a tone list.


### -field AC_DEVCAPFLAGS


<a href="https://msdn.microsoft.com/0c537488-9fb9-4961-bd0a-1937aefc0b08">Device capability flags</a>.


### -field AC_ANSWERMODES


<a href="https://msdn.microsoft.com/35f63d92-970f-4fb8-aba9-179fc7de70f4">Answer modes</a>.


### -field AC_LINEFEATURES

Specifies the features available for this line using the 
<a href="https://msdn.microsoft.com/77fa313c-e720-4607-b691-51b5be76ceed">LINEFEATURE_ constants</a>. Invoking a supported feature requires the line to be in the proper state and the underlying line device to be opened in a compatible mode. A zero in a bit position indicates that the corresponding feature is never available. A one indicates that the corresponding feature may be available if the line is in the appropriate state for the operation to be meaningful. This member allows an application to discover which line features can be (and which can never be) supported by the device.


### -field AC_SETTABLEDEVSTATUS

Indicates 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS_</a> values that can be modified.


### -field AC_PARKSUPPORT

Indicates whether park is supported using the 
<a href="https://msdn.microsoft.com/4b182c16-9d58-4244-bc5a-05c393800948">LINEPARKMODE_</a> flags.


### -field AC_CALLERIDSUPPORT

Identifies support for caller number identification using the 
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_</a> flags.


### -field AC_CALLEDIDSUPPORT

Identifies support for called number identification using the 
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_</a> flags.


### -field AC_CONNECTEDIDSUPPORT

Indicates whether connected ID is supported using the 
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_</a> flags.


### -field AC_REDIRECTIONIDSUPPORT

Indicates whether redirection ID is supported using the 
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_</a> flags.


### -field AC_REDIRECTINGIDSUPPORT

Indicates whether redirecting ID is supported using the 
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_</a> flags.


### -field AC_ADDRESSCAPFLAGS

The address 
<a href="https://msdn.microsoft.com/530af273-82ba-4310-8aac-266d657e1bfe">capability flags</a> describe various Boolean address capabilities. For example, LINEADDRCAPFLAGS_FWDNUMRINGS indicates whether the number of rings for a no-answer can be specified when forwarding on a no-answer.


### -field AC_CALLFEATURES1


<a href="https://msdn.microsoft.com/8bb1d678-079c-4c83-b4a2-08fd7afdca9b">Call feature set one</a>.


### -field AC_CALLFEATURES2


<a href="https://msdn.microsoft.com/67a3b587-dd5b-4ccf-ab69-2137604706b8">Supplemental call features</a> for conferencing, transferring, and parking calls.


### -field AC_REMOVEFROMCONFCAPS

Specifies the address's capabilities for removing calls from a conference call. This member uses the 
<a href="https://msdn.microsoft.com/fa1b36de-8be3-48ae-a58b-800f30259041">LINEREMOVEFROMCONF_ constants</a>.


### -field AC_REMOVEFROMCONFSTATE

Uses the 
<a href="https://msdn.microsoft.com/18d881ee-cf98-4dec-a561-333c2518935d">LINECALLSTATE_ constants</a> to specify the state of the call after it has been removed from a conference call.


### -field AC_TRANSFERMODES


<a href="https://msdn.microsoft.com/0a01131f-b63c-45ef-a0a9-17d69a0dacf9">Transfer modes</a>.


### -field AC_ADDRESSFEATURES

The 
<a href="https://msdn.microsoft.com/dedeee7b-578b-4b19-8b99-5cd23779d661">line address features</a> describe operations that can be invoked on an address. For example, if LINEADDRFEATURE_FORWARD is set, the address can be forwarded.


### -field AC_PREDICTIVEAUTOTRANSFERSTATES

The call state or states upon which a call made by a predictive dialer can be set to automatically transfer the call to another address; one or more of the 
<a href="https://msdn.microsoft.com/18d881ee-cf98-4dec-a561-333c2518935d">LINECALLSTATE_ constants</a>. The value 0 indicates automatic transfer based on call state is unavailable.


### -field AC_MAXCALLDATASIZE

Maximum data block size allowed.


### -field AC_LINEID

Returns the device identifier of the line device with which this address is associated. TAPI 2.1 cross-reference: 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>.


### -field AC_ADDRESSID

Address identifier. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -field AC_FORWARDMODES


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Forwarding modes</a>.


### -field AC_MAXFORWARDENTRIES

The maximum number of different forwarding entries that can be supported by the current address.


### -field AC_MAXSPECIFICENTRIES

Specifies the maximum number of entries that can be set using 
<a href="https://msdn.microsoft.com/5f7972a8-c9b0-4033-8b00-a107a513ee66">ITForwardInformation::SetForwardType</a> that can contain forwarding instructions based on a specific caller (selective call forwarding). This member is zero if selective call forwarding is not supported.


### -field AC_MINFWDNUMRINGS

Specifies the minimum number of rings that can be set to determine when a call is officially considered "no answer."


### -field AC_MAXFWDNUMRINGS

Specifies the maximum number of rings that can be set to determine when a call is officially considered "no answer."


### -field AC_MAXCALLCOMPLETIONS

The maximum number of concurrent call completion requests that can be outstanding on this address. Zero implies that call completion is not available.


### -field AC_CALLCOMPLETIONCONDITIONS


<a href="https://msdn.microsoft.com/0d7b82e8-ce97-410a-a946-30055cd2d558">Call completion conditions</a>.


### -field AC_CALLCOMPLETIONMODES


<a href="https://msdn.microsoft.com/68f755a1-586b-4c5b-b8e8-c8b40eb71685">Call completion modes</a>.


### -field AC_PERMANENTDEVICEID

The permanent identifier by which the line device is known in the system's configuration. This value does not change as lines are added and removed from the system. It can therefore be used to link line-specific information in the registry or other files in a way that is not affected by changes in other lines. If a line has more than one address, all addresses will have the same permanent device identifier. TSP writers should note that this value must be preserved across operating system upgrades.


### -field AC_GATHERDIGITSMINTIMEOUT


### -field AC_GATHERDIGITSMAXTIMEOUT


### -field AC_GENERATEDIGITMINDURATION


### -field AC_GENERATEDIGITMAXDURATION


### -field AC_GENERATEDIGITDEFAULTDURATION




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/76e61d5e-48b6-4b9c-9076-bd20a794859c">ITAddressCapabilities::get_AddressCapability</a>
 

 

