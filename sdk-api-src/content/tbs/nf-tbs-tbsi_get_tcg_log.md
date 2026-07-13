---
UID: NF:tbs.Tbsi_Get_TCG_Log
title: Tbsi_Get_TCG_Log function (tbs.h)
description: Retrieves the most recent Windows Boot Configuration Log (WBCL), also referred to as a TCG log.
helpviewer_keywords: ["Tbsi_Get_TCG_Log","Tbsi_Get_TCG_Log function [TBS]","tbs.tbsi_get_tcg_log","tbs/Tbsi_Get_TCG_Log"]
old-location: tbs\tbsi_get_tcg_log.htm
tech.root: TBS
ms.assetid: f52c71fd-383b-4c32-9b49-8904ffb692c1
ms.date: 12/05/2018
ms.keywords: Tbsi_Get_TCG_Log, Tbsi_Get_TCG_Log function [TBS], tbs.tbsi_get_tcg_log, tbs/Tbsi_Get_TCG_Log
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsi_Get_TCG_Log
 - tbs/Tbsi_Get_TCG_Log
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsi_Get_TCG_Log
---

# Tbsi_Get_TCG_Log function


## -description

Retrieves the most recent Windows Boot Configuration Log (WBCL), also referred to as a TCG log.

## -parameters

### -param hContext [in]

The TBS handle of the context that is retrieving the log. You get this parameter from a previous call to the <a href="/windows/desktop/api/tbs/nf-tbs-tbsi_context_create">Tbsi_Context_Create</a> function.

### -param pOutputBuf [out]

A pointer to a buffer to receive  and store the WBCL. This parameter may be NULL to estimate the required buffer when the location pointed to by <i>pcbOutput</i> is also 0 on input.

### -param pOutputBufLen [in, out]

A pointer to an unsigned long integer that, on input, specifies the size, in bytes, of the output buffer.  If the function succeeds, this parameter, on output, receives the size, in bytes, of the data pointed to by <i>pOutputBuf</i>. If the function fails, this parameter does not receive a value.

Calling the <b>Tbsi_Get_TCG_Log</b> function with a zero length buffer will return the size of the buffer required. <b>Windows Vista with SP1 and Windows Server 2008:  </b>This functionality is not available.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INTERNAL_ERROR</b></dt>
<dt>2150121473 (0x80284001)</dt>
</dl>
</td>
<td width="60%">
An internal software error occurred. 

<div class="alert"><b>Note</b>  If TBS_E_INTERNAL_ERROR is returned, the system event log may contain event ID 16385 from the TBS event source with error code 0x80070032.  This may indicate that the hardware platform does not provide a TCG event log to the operating system.  Sometimes this can be resolved by installing a BIOS upgrade from the platform manufacturer.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_OUTPUT_POINTER</b></dt>
<dt>2150121475 (0x80284003)</dt>
</dl>
</td>
<td width="60%">
A specified output pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_CONTEXT</b></dt>
<dt>2150121476 (0x80284004)</dt>
</dl>
</td>
<td width="60%">
The specified context handle does not refer to a valid context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INSUFFICIENT_BUFFER</b></dt>
<dt>2150121477 (0x80284005)</dt>
</dl>
</td>
<td width="60%">
The output buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_BUFFER_TOO_LARGE</b></dt>
<dt>2150121486 (0x8028400E)</dt>
</dl>
</td>
<td width="60%">
The output buffer is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_TPM_NOT_FOUND</b></dt>
<dt>2150121487 (0x8028400F)</dt>
</dl>
</td>
<td width="60%">
A compatible Trusted Platform Module (TPM) Security Device cannot be found on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_DEACTIVATED</b></dt>
<dt>2150121494 (0x80284016)</dt>
</dl>
</td>
<td width="60%">
The Trusted Platform Module (TPM) Security Device is deactivated.

<b>Windows Vista with SP1 and Windows Server 2008:  </b>This return value is not available.

</td>
</tr>
</table>

## -remarks

The <b>Tbsi_Get_TCG_Log</b> function returns the TCG Event Log for the system, and the buffer size depends on the number of events.

<b>Windows 10:  </b><p class="note">The function may return a log that uses a format that is compatible with different hashing algorithms, depending on hardware capabilities and firmware settings. This log formats each event except the first as a TCG_PCR_EVENT2 structure:


```
typedef struct {
  TCG_PCRINDEX PCRIndex;
  TCG_EVENTTYPE EventType;
  TPML_DIGEST_VALUES Digests;
  UINT32 EventSize;
  UINT8 Event[EventSize];
} TCG_PCR_EVENT2;

typedef struct {
  UINT32 Count;
  TPMT_HA Digests;
} TPML_DIGEST_VALUES;

typedef struct {
  UINT16 HashAlg;
  UINT8 Digest[size_varies_with_algorithm];
} TPMT_HA;

```


<p class="note">The log formats the first event as a <b>TCG_PCR_EVENT</b> structure, which is described later in this Remarks section. The following table describes the values of the members of this structure for this first event.

<table>
<tr>
<th>TCG_PCR_EVENT member</th>
<th>Value or description</th>
</tr>
<tr>
<td><b>PCRIndex</b></td>
<td>0</td>
</tr>
<tr>
<td><b>EventType</b></td>
<td>EV_NO_ACTION</td>
</tr>
<tr>
<td><b>Digest</b></td>
<td>20 bytes of zeros</td>
</tr>
<tr>
<td><b>EventSize</b></td>
<td>The size of the <b>Event</b> member</td>
</tr>
<tr>
<td><b>Event</b></td>
<td>Has a type of <b>TCG_EfiSpecIdEventStruct</b></td>
</tr>
</table>
 

<p class="note">The following shows the syntax of the <b>TCG_EfiSpecIdEventStruct</b> structure that the <b>Event</b> member of the <b>TCG_PCR_EVENT</b> structure uses for the first log event.


```
typedef struct {
  BYTE[16] Signature;
  UINT32 PlatformClass;
  UINT8 SpecVersionMinor;
  UINT8 SpecVersionMajor;
  UINT8 SpecErrata;
  UINT8 UintNSize;
  UINT32 NumberOfAlgorithms;
  TCG_EfiSpecIdEventAlgorithmSize DigestSizes[NumberOfAlgorithms];
  UINT8 VendorInfoSize;
  UINT8 VendorInfo[VendorInfoSize];
} TCG_EfiSpecIdEventStruct;

typedef struct {
  UINT16 HashAlg;
  UINT16 DigestSize;
} TCG_EfiSpecIdEventAlgorithmSize;

```


<p class="note">The <b>Signature</b> member of the <b>TCG_EfiSpecIdEventStruct</b> structure is set to a null-terminated ASCII string of "Spec ID Event03" when the log uses the format that is compatible with different hashing algorithms. The <b>DigestSizes</b> array in this first event contains the digest sizes for the different hashing algorithms that the log uses. When a parser inspects an event of type <b>TCG_PCR_EVENT2</b>, the parser can parse the <b>TPML_DIGEST_VALUES</b> member without information about all of the hashing algorithms present. The digest sizes in the first event allow the parser to skip the correct number of bytes for the  digests that are present.

<p class="note">If the <b>Signature</b> member is not set to a null-terminated ASCII string of "Spec ID Event03", then the events in the log are of type <b>TCG_PCR_EVENT</b>, and the <b>TCG_EfiSpecIdEventStruct</b> structure does not contain the <b>NumberOfAlgorithms</b> and <b>DigestSizes</b> members.

 



<p class="note">The log format that is compatible with different hashing algorithms allows the platform and operating system to use SHA1, SHA256, or other hashing algorithms. If the platform supports the SHA256 hashing algorithm and the uses the log format that is compatible with different hashing algorithms, the platform uses the SHA256 algorithm instead of  SHA1.




<b>Windows Vista with SP1 and Windows Server 2008:  </b>The function returns the log directly from the ACPI table and returns the entire ACPI allocated buffer, including the unused buffer after any events.

The Windows-defined events in the TCG event log are a tuple of {Type, Length, Value}. You can parse the log using the following TCG_PCR_EVENT structure from the <a href="https://trustedcomputinggroup.org">TCG PC Client spec</a>. You can create a correlation between lists of log events using the information in the <a href="https://www.microsoft.com/download/details.aspx?id=52487&from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fdownloads%2F74c45746-24ad-4cb7-ba4b-0c6df2f92d5d%2F">TPM PCP Toolkit</a> and the <a href="https://trustedcomputinggroup.org">TPM Main Specification</a>. 


```
typedef struct {
  TCG_PCRINDEX PCRIndex;
  TCG_EVENTTYPE EventType;
  TCG_DIGEST Digest;
  UINT32 EventSize;
  UINT8 Event[EventSize];
} TCG_PCR_EVENT;
```




The memory size required for the <i>pOutputBuf</i> parameter should either be the constant in <b>TBS_IN_OUT_BUF_SIZE_MAX</b>, defined in the Tbs.h header file, or it should be obtained by calling the <b>Tbsi_Get_TCG_Log</b> function with a zero length buffer to get the required buffer size.


<b>Windows Vista with SP1 and Windows Server 2008:  </b>Calling the <b>Tbsi_Get_TCG_Log</b> function with a zero length buffer to get the required buffer size is not supported. We recommend that you use the constant <b>TBS_IN_OUT_BUF_SIZE_MAX</b>, defined in the Tbs.h header file, for the memory size for the <i>pOutputBuf</i> parameter.




#### Examples


```cpp
#include <windows.h>
#include <tbs.h>
#pragma comment(lib, "Tbs.lib")

void main()
{
    TBS_RESULT result;
    TBS_HCONTEXT hContext;
    TBS_CONTEXT_PARAMS contextParams;
    contextParams.version = TBS_CONTEXT_VERSION_ONE;
    result = Tbsi_Context_Create(&contextParams, &hContext);
    if (result == TBS_SUCCESS) 
    {
        UINT32 iLogSize = TBS_IN_OUT_BUF_SIZE_MAX;
        BYTE* pLogBuffer = new BYTE[iLogSize];
        result = Tbsi_Get_TCG_Log(hContext, pLogBuffer, &iLogSize);
    }
}

```