---
UID: NF:ntmsapi.UpdateNtmsOmidInfo
title: UpdateNtmsOmidInfo function
author: windows-driver-content
description: The UpdateNtmsOmidInfo function updates the RSM database with label information immediately after writing to the newly allocated medium.
old-location: fs\updatentmsomidinfo.htm
old-project: Rsm
ms.assetid: 2e154005-a14c-4de6-aec5-f30b934c64a2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: NTMS_OMID_TYPE_FILESYSTEM_INFO, NTMS_OMID_TYPE_RAW_LABEL, UpdateNtmsOmidInfo, UpdateNtmsOmidInfo function [Files], _zaw_updatentmsomidinfo, base.updatentmsomidinfo, fs.updatentmsomidinfo, ntmsapi/UpdateNtmsOmidInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntmsapi.dll
api_name:
-	UpdateNtmsOmidInfo
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# UpdateNtmsOmidInfo function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>UpdateNtmsOmidInfo</b> function updates the RSM database with label information immediately after writing to the newly allocated medium.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaId [in]

Unique identifier of a piece of logical media.


### -param labelType [in]

Label type. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OMID_TYPE_FILESYSTEM_INFO"></a><a id="ntms_omid_type_filesystem_info"></a><dl>
<dt><b>NTMS_OMID_TYPE_FILESYSTEM_INFO</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffer</i> parameter contains an NTMS_FILESYSTEM_INFO structure. This flag is used for media that contain file systems.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OMID_TYPE_RAW_LABEL"></a><a id="ntms_omid_type_raw_label"></a><dl>
<dt><b>NTMS_OMID_TYPE_RAW_LABEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffer</i> parameter contains the raw bytes of the application label. This flag is used for media that contain application written labels.

</td>
</tr>
</table>
 


### -param numberOfBytes [in]

Number of bytes sent in the <i>lpBuffer</i> parameter.


### -param lpBuffer [in]

Label information. The format of this parameter depends on the value of the <i>labelType</i> parameter.


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
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
Unable to retrieve the logical media definition from the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
Unable to retrieve the side definition from the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpMediaId</i> parameter is <b>NULL</b>.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



The application updates RSM with the information supplied by the 
<b>UpdateNtmsOmidInfo</b> function and RSM verifies the information in the database. The label information is stored in the RSM database with the side associated with this LMID.

The 
<b>UpdateNtmsOmidInfo</b> function must be executed on the RSM server. Remote execution of this function results in an error.

For tape media <i>lpBuffer</i> must point to a buffer that holds the label just written on the tape. The data in this buffer is passed directly to the ClaimMediaLabel entry point of each MLL. One of the installed MLLs must recognize a valid label in this data.

For media with file systems, <i>lpBuffer</i> must be a pointer to a buffer that contains the following structure: 

<pre class="syntax" xml:space="preserve"><code>
typedef struct {
    WCHAR   FileSystemType[64];
    WCHAR   VolumeName[256];
    DWORD   SerialNumber;
} NTMS_FILESYSTEM_INFO;</code></pre>
RSM uses this file system info as the OMID. The format utilities (LDM, explorer, format.com, and so on) effectively performs the same functionality as this call. An application that performs its own formatting or formats with a third-party file system type should only need to call 
<b>UpdateNtmsOmidInfo</b> for file system media.




## -see-also




<a href="removable_storage_manager_functions.htm">On-Media-Identifier Management Functions</a>
 

 

