---
UID: NF:lpmapi.LPM_DeleteState
title: LPM_DeleteState function
author: windows-sdk-content
description: The LPM_DeleteState function is called by the PCM to delete the LPMs' RSVP state information.
old-location: qos\lpm_deletestate.htm
old-project: QOS
ms.assetid: 54251572-22a6-4652-a88c-7ed696911c18
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: ADM_CTRL_FAILED, FLOW_DURATION, LPM_DeleteState, LPM_DeleteState callback, LPM_DeleteState callback function [QOS], RCVD_PATH_TEAR, RCVD_RESV_TEAR, STATE_TIMEOUT, _gqos_lpm_deletestate, lpmapi/LPM_DeleteState, qos.lpm_deletestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_DeleteState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LPM_DeleteState function


## -description


The 
<i>LPM_DeleteState</i> function is called by the PCM to delete the LPMs' RSVP state information. RSVP states are deleted on various occasions, including when the SBM receives RSVP TEAR/ERR messages, or when an RSVP state times out. The 
<i>LPM_DeleteState</i> function call is synchronous. The PCM does not expect any results from the LPM for this request.


## -parameters




### -param pRcvdIfAddr [in]

Pointer to the interface on which the RSVP TEAR message was received. The received interface IP address is supplied as the RSVP HOP object, and the Logical Interface Handle is set to the SNMP Index. If the PCM is calling the 
<i>LPM_DeleteState</i> function for any reason other than an RSVP TEAR message, this parameter can be null. Note that interface index numbers can change with the addition and deletion of interfaces, due to the Plug and Play features of Windows 2000.


### -param RsvpMsgType [in]

RSVP message type for which the LPM should delete its state.


### -param pRsvpSession [in]

Pointer to the RSVP session object for which the LPM should delete its state. This value is never null.


### -param pRsvpFromHop [in]

Pointer to an 
RSVP HOP object identifying the node that sent the TEAR message. LPMs can use this parameter to locate state information.


### -param pResvStyle [in]

Pointer to an argument that specifies the RSVP reservation style for RSVP RESV_TEAR messages. LPMs can use this parameter to locate state information.


### -param FilterSpecCount [in]

Specifies the number of FilterSpecs in <i>FilterSpecList</i>. For RESV messages, <i>FilterSpecCount</i> is dependent on <i>RsvpStyle</i>. For PATH messages, this value will always be 1.


### -param ppFilterSpecList [in]

Array of FilterSpec pointers. Note that the contents of <i>FilterSpecList</i> is dependent on <i>RsvpStyle</i>; if <i>RsvpMsgType</i> is RSVP_PATH then <i>FilterSpecList</i> specifies the SenderTemplate, if <i>RsvpMsgType</i> is RSVP_RESV then <i>FilterSpecList</i> is the list of filters for which the RESV state needs to be deleted.


### -param TearDownReason [in]

Reason for deleting the state. Possible values are:

<a id="RCVD_PATH_TEAR"></a>
<a id="rcvd_path_tear"></a>


#### RCVD_PATH_TEAR

<a id="RCVD_RESV_TEAR"></a>
<a id="rcvd_resv_tear"></a>


#### RCVD_RESV_TEAR

<a id="ADM_CTRL_FAILED"></a>
<a id="adm_ctrl_failed"></a>


#### ADM_CTRL_FAILED

<a id="STATE_TIMEOUT"></a>
<a id="state_timeout"></a>


#### STATE_TIMEOUT

<a id="FLOW_DURATION"></a>
<a id="flow_duration"></a>


#### FLOW_DURATION

LPMs can use <i>DeleteReason</i> for statistical gathering or any other use.


## -returns



This callback function does not return a value.




## -remarks



The PCM will call the 
<i>LPM_DeleteState</i> function for each LPM; LPMs should be prepared to handle 
<i>LPM_DeleteState</i> for a nonexistent state, as described further in the Remarks section of the 
<a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a>
 

 

