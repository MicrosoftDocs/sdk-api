---
UID: NF:tbs.Tbsi_Get_TCG_Log_Ex
title: Tbsi_Get_TCG_Log_Ex function (tbs.h)
description: Gets the Windows Boot Configuration Log (WBCL), also referred to as the TCG log, of the specified type.
helpviewer_keywords: ["TBS_TCGLOG_DRTM_CURRENT","TBS_TCGLOG_SRTM_BOOT","TBS_TCGLOG_SRTM_CURRENT","TBS_TCGLOG_SRTM_RESUME","Tbsi_Get_TCG_Log_Ex","Tbsi_Get_TCG_Log_Ex function [TBS]","tbs.tbsi_get_tcg_log_ex","tbs/Tbsi_Get_TCG_Log_Ex"]
old-location: tbs\tbsi_get_tcg_log_ex.htm
tech.root: TBS
ms.assetid: 7895D501-97A7-4813-B997-B7D8C6F7C0C6
ms.date: 12/05/2018
ms.keywords: TBS_TCGLOG_DRTM_CURRENT, TBS_TCGLOG_SRTM_BOOT, TBS_TCGLOG_SRTM_CURRENT, TBS_TCGLOG_SRTM_RESUME, Tbsi_Get_TCG_Log_Ex, Tbsi_Get_TCG_Log_Ex function [TBS], tbs.tbsi_get_tcg_log_ex, tbs/Tbsi_Get_TCG_Log_Ex
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - Tbsi_Get_TCG_Log_Ex
 - tbs/Tbsi_Get_TCG_Log_Ex
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
 - Tbsi_Get_TCG_Log_Ex
---

# Tbsi_Get_TCG_Log_Ex function


## -description

Gets the Windows Boot Configuration Log (WBCL), also referred to as the TCG log, of the specified type.

## -parameters

### -param logType [in]

The type of log to retrieve.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBS_TCGLOG_SRTM_CURRENT"></a><a id="tbs_tcglog_srtm_current"></a><dl>
<dt><b>TBS_TCGLOG_SRTM_CURRENT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The log associated with PCRs 0-15 for the current session (boot or resume).

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_TCGLOG_DRTM_CURRENT"></a><a id="tbs_tcglog_drtm_current"></a><dl>
<dt><b>TBS_TCGLOG_DRTM_CURRENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The log associated with PCRs 17-22 for the current session (boot or resume).

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_TCGLOG_SRTM_BOOT"></a><a id="tbs_tcglog_srtm_boot"></a><dl>
<dt><b>TBS_TCGLOG_SRTM_BOOT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The log associated with PCRs 0-15 for the most recent clean boot session.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_TCGLOG_SRTM_RESUME"></a><a id="tbs_tcglog_srtm_resume"></a><dl>
<dt><b>TBS_TCGLOG_SRTM_RESUME</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The log associated with PCRs 0-15 for the most recent resume from hibernation.

</td>
</tr>
</table>

### -param pbOutput [out, optional]

                Pointer to a buffer that receives and stores the WBCL. Set to <b>NULL</b> to estimate the required buffer when the location pointed to by <i>pcbOutput</i> is also 0 on input.

### -param pcbOutput [in, out]

Pointer to an unsigned long integer that specifies the size, in bytes, of the output buffer. On success, contains the size, in bytes, of the data pointed to by <i>pOutput</i>. On failure, does not contain a value.

<b>Note</b>  If <i>pbOutput</i> is <b>NULL</b> and the location pointed to by <i>pcbOutput</i> is 0, the function returns <b>TBS_E_BUFFER_TOO_SMALL</b>. In that case, <i>pcbOutput</i> will point to the required size of <i>pbOutput</i>.

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
<dt><b>TBS_E_NO_EVENT_LOG</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
<b>TBS_TCGLOG_DRTM_CURRENT</b> was requested but DRTM was not enabled on the system when the system booted.

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

<div class="alert"><b>Note</b>  If <b>TBS_E_INTERNAL_ERROR</b> is returned, the system event log may contain event ID 16385 from the TBS event source with error code 0x80070032.  This may indicate that the hardware platform does not provide a TCG event log to the operating system.  Sometimes this can be resolved by installing a BIOS upgrade from the platform manufacturer.</div>
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

</td>
</tr>
</table>

## -remarks

The <b>Tbsi_Get_TCG_Log_Ex</b> function returns the TCG Event Log for the system, and the buffer size depends on the number of events.

The function may return a log that uses a format that is compatible with different hashing algorithms, depending on hardware capabilities and firmware settings. This log formats each event except the first as a TCG_PCR_EVENT2 structure:


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


The log formats the first event as a <b>TCG_PCR_EVENT</b> structure, which is described later in this Remarks section. The following table describes the values of the members of this structure for this first event.

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
 

The following shows the syntax of the <b>TCG_EfiSpecIdEventStruct</b> structure that the <b>Event</b> member of the <b>TCG_PCR_EVENT</b> structure uses for the first log event.


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


The <b>Signature</b> member of the <b>TCG_EfiSpecIdEventStruct</b> structure is set to a null-terminated ASCII string of "Spec ID Event03" when the log uses the format that is compatible with different hashing algorithms. The <b>DigestSizes</b> array in this first event contains the digest sizes for the different hashing algorithms that the log uses. When a parser inspects an event of type <b>TCG_PCR_EVENT2</b>, the parser can parse the <b>TPML_DIGEST_VALUES</b> member without information about all of the hashing algorithms present. The digest sizes in the first event allow the parser to skip the correct number of bytes for the  digests that are present.

If the <b>Signature</b> member is not set to a null-terminated ASCII string of "Spec ID Event03", then the events in the log are of type <b>TCG_PCR_EVENT</b>, and the <b>TCG_EfiSpecIdEventStruct</b> structure does not contain the <b>NumberOfAlgorithms</b> and <b>DigestSizes</b> members.

 



The log format that is compatible with different hashing algorithms allows the platform and operating system to use SHA1, SHA256, or other hashing algorithms. If the platform supports the SHA256 hashing algorithm and the uses the log format that is compatible with different hashing algorithms, the platform uses the SHA256 algorithm instead of  SHA1.


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




The memory size required for the <i>pOutputBuf</i> parameter should either be the constant in <b>TBS_IN_OUT_BUF_SIZE_MAX</b>, defined in the Tbs.h header file, or it should be obtained by calling the <b>Tbsi_Get_TCG_Log_Ex</b> function with a zero length buffer to get the required buffer size.

