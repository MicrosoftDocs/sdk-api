---
UID: NF:wdsclientapi.WdsCliInitializeLog
title: WdsCliInitializeLog function (wdsclientapi.h)
description: Initializes logging for the WDS client.
helpviewer_keywords: ["PROCESSOR_ARCHITECTURE_AMD64","PROCESSOR_ARCHITECTURE_IA64","PROCESSOR_ARCHITECTURE_INTEL","WdsCliInitializeLog","WdsCliInitializeLog function [Windows Deployment Services]","wds.wdscliinitializelog","wdsclientapi/WdsCliInitializeLog"]
old-location: wds\wdscliinitializelog.htm
tech.root: wds
ms.assetid: 9d5ad574-a2b6-49cc-8783-4947c3d81d25
ms.date: 12/05/2018
ms.keywords: PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, WdsCliInitializeLog, WdsCliInitializeLog function [Windows Deployment Services], wds.wdscliinitializelog, wdsclientapi/WdsCliInitializeLog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliInitializeLog
 - wdsclientapi/WdsCliInitializeLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliInitializeLog
---

# WdsCliInitializeLog function


## -description

Initializes logging for the WDS client.

## -parameters

### -param hSession [in]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a> function.

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

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>