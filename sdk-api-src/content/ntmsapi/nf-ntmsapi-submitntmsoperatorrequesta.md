---
UID: NF:ntmsapi.SubmitNtmsOperatorRequestA
title: SubmitNtmsOperatorRequestA function (ntmsapi.h)
description: The SubmitNtmsOperatorRequest function submits an RSM operator request. (ANSI)
helpviewer_keywords: ["NTMS_OPREQ_CLEANER", "NTMS_OPREQ_DEVICESERVICE", "NTMS_OPREQ_MESSAGE", "NTMS_OPREQ_MOVEMEDIA", "NTMS_OPREQ_NEWMEDIA", "SubmitNtmsOperatorRequestA", "ntmsapi/SubmitNtmsOperatorRequestA"]
old-location: fs\submitntmsoperatorrequest.htm
tech.root: fs
ms.assetid: d2c146d0-f1f9-4810-a489-91b5c4ca3431
ms.date: 12/05/2018
ms.keywords: NTMS_OPREQ_CLEANER, NTMS_OPREQ_DEVICESERVICE, NTMS_OPREQ_MESSAGE, NTMS_OPREQ_MOVEMEDIA, NTMS_OPREQ_NEWMEDIA, SubmitNtmsOperatorRequest, SubmitNtmsOperatorRequest function [Files], SubmitNtmsOperatorRequestA, SubmitNtmsOperatorRequestW, _zaw_submitntmsoperatorrequest, base.submitntmsoperatorrequest, fs.submitntmsoperatorrequest, ntmsapi/SubmitNtmsOperatorRequest, ntmsapi/SubmitNtmsOperatorRequestA, ntmsapi/SubmitNtmsOperatorRequestW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SubmitNtmsOperatorRequestW (Unicode) and SubmitNtmsOperatorRequestA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SubmitNtmsOperatorRequestA
 - ntmsapi/SubmitNtmsOperatorRequestA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - SubmitNtmsOperatorRequest
 - SubmitNtmsOperatorRequestA
 - SubmitNtmsOperatorRequestW
---

# SubmitNtmsOperatorRequestA function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SubmitNtmsOperatorRequest</b> function submits an RSM operator request.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param dwRequest [in]

Type of operator request. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_CLEANER"></a><a id="ntms_opreq_cleaner"></a><dl>
<dt><b>NTMS_OPREQ_CLEANER</b></dt>
</dl>
</td>
<td width="60%">
RSM sends an operator request to insert a cleaner when a clean operation is queued and no cleaner is available to the drive. The <i>lpArg1Id</i> parameter can be either a library or slot identifier.

 Requires NTMS_CONTROL_ACCESS to the library.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_DEVICESERVICE"></a><a id="ntms_opreq_deviceservice"></a><dl>
<dt><b>NTMS_OPREQ_DEVICESERVICE</b></dt>
</dl>
</td>
<td width="60%">
An application or RSM sends an operator request for drive service when a changer device or drive is experiencing problems. The <i>lpArg1Id</i> parameter specifies the device that needs service. This parameter can be an iedoor, library, physical media, or drive identifier.

 Requires NTMS_CONTROL_ACCESS to the library.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_MESSAGE"></a><a id="ntms_opreq_message"></a><dl>
<dt><b>NTMS_OPREQ_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
Application message only.

 Requires NTMS_USE_ACCESS to the computer.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_MOVEMEDIA"></a><a id="ntms_opreq_movemedia"></a><dl>
<dt><b>NTMS_OPREQ_MOVEMEDIA</b></dt>
</dl>
</td>
<td width="60%">
An application or RSM sends an operator request to move media from one library to another for a mount of offline media or to eject existing media to the offline library. The <i>lpArg1Id</i> parameter specifies the piece of physical media that must be moved and the <i>lpArg2Id</i> parameter specifies the target library.

 Requires NTMS_CONTROL_ACCESS to the media pool.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_NEWMEDIA"></a><a id="ntms_opreq_newmedia"></a><dl>
<dt><b>NTMS_OPREQ_NEWMEDIA</b></dt>
</dl>
</td>
<td width="60%">
An application or RSM sends an operator request for new media when no media is available. The <i>lpArg1Id</i> parameter specifies the media pool object and the <i>lpArg2Id</i> parameter is the optional library identifier to which to add the new medium.

 Requires NTMS_CONTROL_ACCESS to the media pool.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
</table>

### -param lpMessage [in]

Optional message string to be sent to the user.

### -param lpArg1Id [in]

Object identifier for the operator request. Refer to the descriptions of the values in the <i>dwRequest</i> parameter for a description of what type of object must be passed for this parameter.

### -param lpArg2Id [in]

Object identifier for the operator request. Refer to the descriptions of the values in the <i>dwRequest</i> parameter for details on what type of object must be passed for this parameter.

### -param lpRequestId [out]

Pointer to a buffer that receives the identifier of the operator request that was created.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database query or update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the source or destination object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>

## -remarks

The 
<b>SubmitNtmsOperatorRequest</b> function submits an operator request and returns the status of the request (Satisfied or Canceled) or times out (if the operator does not act upon the request). Operator requests are used to request media, to request that the specified medium be moved from one library to another, or to request RSM device service.

The NTMS_OPEREQ_MESSAGE value (in the <i>dwRequest</i> parameter) is the request type most often used by applications. RSM cannot use NTMS_OPEREQ_MESSAGE. RSM uses the other request types as needed.





> [!NOTE]
> The ntmsapi.h header defines SubmitNtmsOperatorRequest as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cancelntmsoperatorrequest">CancelNtmsOperatorRequest</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-mountntmsmedia">MountNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Operator Request Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-satisfyntmsoperatorrequest">SatisfyNtmsOperatorRequest</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsoperatorrequest">WaitForNtmsOperatorRequest</a>
