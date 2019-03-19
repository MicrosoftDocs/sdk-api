---
UID: NF:wdsclientapi.WdsCliInitializeLog
title: WdsCliInitializeLog function (wdsclientapi.h)
author: windows-sdk-content
description: Initializes logging for the WDS client.
old-location: wds\wdscliinitializelog.htm
tech.root: wds
ms.assetid: 9d5ad574-a2b6-49cc-8783-4947c3d81d25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, WdsCliInitializeLog, WdsCliInitializeLog function [Windows Deployment Services], wds.wdscliinitializelog, wdsclientapi/WdsCliInitializeLog
ms.topic: function
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliInitializeLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliInitializeLog function


## -description


Initializes logging for the WDS client.


## -parameters




### -param hSession [in]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a> function.


### -param ulClientArchitecture [in]

A constant that identifies the processor architecture of the client.


This parameter can have one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_AMD64"></a><a id="processor_architecture_amd64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_AMD64</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The image is an x64 image (AMD AMD64 or Intel EM64T).

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_IA64"></a><a id="processor_architecture_ia64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_IA64</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The image is an Itanium-based system image.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_INTEL"></a><a id="processor_architecture_intel"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_INTEL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The image is a 32-bit Intel x86 image.

</td>
</tr>
</table>
 


### -param pwszClientId [in]

A pointer to a string value that contains a GUID that represents this WDS client. This is typically the GUID for the System Management BIOS (SMBIOS.)


### -param pwszClientAddress [in]

A pointer to a string value that contains the network address of the WDS client. This is typically the IP address in string form, for example, 
      "127.0.0.1".


## -returns



If the function succeeds, the return is <b>S_OK</b>. 

If logging has already been initialize for the session, the return value is 
      <b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b>.




## -see-also




<a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a>



<a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a>



<a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

