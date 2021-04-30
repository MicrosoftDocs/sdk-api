---
UID: NC:lpmapi.CBGETRSVPOBJECTS
title: CBGETRSVPOBJECTS (lpmapi.h)
description: The cbGetRsvpObjects function is a callback function for LPMs to asynchronously return results for LPM_GetRsvpObjects requests.
helpviewer_keywords: ["CBGETRSVPOBJECTS","CBGETRSVPOBJECTS callback function [QOS]","_gqos_cbpgetrsvpobjects","cbGetRsvpObjects","cbGetRsvpObjects callback","cbGetRsvpObjects callback function [QOS]","lpmapi/cbGetRsvpObjects","qos.cbgetrsvpobjects","qos.cbpgetrsvpobjects"]
old-location: qos\cbgetrsvpobjects.htm
tech.root: QOS
ms.assetid: baedb3e9-7768-4666-8bd7-78dd1d0eb0de
ms.date: 12/05/2018
ms.keywords: CBGETRSVPOBJECTS, CBGETRSVPOBJECTS callback function [QOS], _gqos_cbpgetrsvpobjects, cbGetRsvpObjects, cbGetRsvpObjects callback, cbGetRsvpObjects callback function [QOS], lpmapi/cbGetRsvpObjects, qos.cbgetrsvpobjects, qos.cbpgetrsvpobjects
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CBGETRSVPOBJECTS
 - lpmapi/CBGETRSVPOBJECTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - CBGETRSVPOBJECTS
---

## -description

The <i>cbGetRsvpObjects</i> function is a callback function for LPMs to asynchronously return results for 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_getrsvpobjects">LPM_GetRsvpObjects</a> requests. LPMs call the 
<i>cbGetRsvpObjects</i> function to asynchronously return policy data objects to the PCM for an 
<i>LPM_GetRsvpObjects</i> request. An LPM should only use the 
<i>cbGetRsvpObjects</i> function if it returned LPM_RESULTS_DEFER to the PCM's 
<i>LPM_GetRsvpObjects</i> request.

## -parameters

### -param LpmHandle [in]

Unique handle for the LPM, as supplied in 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>. The PCM will ignore any result that is not accompanied by a valid handle.

### -param RequestHandle [in]

Unique handle that distinguishes this request from all other requests, provided from the corresponding 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_getrsvpobjects">LPM_GetRsvpObjects</a> request.

### -param LpmError [in]

Error value, used by the PCM to determine whether the policy data objects returned with this function should be used. Any value other than LPM_OK will result in the PCM ignoring the contents of *<i>RsvpObjects</i>. 

Note that if an LPM is returning an error, it should free buffers allocated during the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_getrsvpobjects">LPM_GetRsvpObjects</a> request processing; these buffers should have been allocated using the <b>MemoryAllocator</b> function, supplied within the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function as its <i>FreeMemory</i> parameter.

If no policy data objects are being returned, <i>LpmError</i> must be set to LPM_OK, <i>RsvpObjectsCount</i> must be set to zero, and *<i>RsvpObjects</i> must be set to null. The LPM can force the SBM to stop sending out the RSVP message by setting the value of <i>LpmError</i> to LPV_DROP_MSG.

### -param RsvpObjectsCount [in]

Number of policy data objects being returned. If no policy data objects are being returned, the <i>LpmError</i> parameter must be set to LPM_OK, the <i>RsvpObjectsCount</i> parameter must be set to zero, and the *<i>RsvpObjects</i> parameter must be set to null.

### -param ppRsvpObjects [in]

Array of pointers to policy data object. The buffer containing the policy data objects should be allocated using the <b>MemoryAllocator</b> function supplied within the <a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function. The Subnet Bandwidth Manager (SBM) will free the policy data objects when they are no longer needed. 

If no policy data objects are being returned, <i>LpmError</i> must be set to LPM_OK, <i>RsvpObjectsCount</i> must be set to zero, and *<i>RsvpObjects</i> must be set to null.

## -returns

Return values are defined by the application providing the callback.

## -remarks

LPMs do not need to send policy data options if only default options are required. Since the content of policy data objects are opaque to the PCM, no host-to-network order conversion of policy element headers and contents will be done by the PCM; the PCM expects LPMs to generate policy elements in the network order such that the receiver of the policy elements can correctly parse them. However, the policy data object header must be in host order to allow the PCM to merge policy elements (if possible or applicable).

From LPMs that support all PE types, the PCM expects complete policy data objects and their required policy data options. Furthermore, the PCM expects the policy data object header to be in host order; it is the responsibility of the LPM to process the host-to-network order conversions of policy options and policy elements.

If any LPM returns LPV_DROP_MSG, the SBM will not send out an RSVP refresh message, but will free the policy data objects returned by other LPMs (those that did not return LPV_DROP_MSG, if any). By not sending out RSVP refresh messages, a flow's RSVP state both upstream and downstream will begin to age, and eventually get deleted.

<div class="alert"><b>Note</b>  The SBM will send out the RSVP refresh message even if some or all LPMs fail to return policy data objects in a timely fashion, even though such an outgoing RSVP message may not contain all policy data objects it should.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_getrsvpobjects">LPM_GetRsvpObjects</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>
