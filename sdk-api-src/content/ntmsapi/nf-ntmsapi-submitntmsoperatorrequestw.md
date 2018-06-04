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

# SubmitNtmsOperatorRequestW function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SubmitNtmsOperatorRequest</b> function submits an RSM operator request.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


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




## -see-also




<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a>



<a href="https://msdn.microsoft.com/d0ba65fe-0355-4bd6-b9ad-98e8f7992827">CancelNtmsOperatorRequest</a>



<a href="https://msdn.microsoft.com/f943f36c-654a-48ed-aeb2-1fc146f2d9ff">MountNtmsMedia</a>



<a href="removable_storage_manager_functions.htm">Operator Request Functions</a>



<a href="https://msdn.microsoft.com/37f9c9c4-7fb2-4559-94a4-e508b277e69e">SatisfyNtmsOperatorRequest</a>



<a href="https://msdn.microsoft.com/abc78047-a6d7-4e98-baec-5e4ba394c64f">WaitForNtmsOperatorRequest</a>
 

 

