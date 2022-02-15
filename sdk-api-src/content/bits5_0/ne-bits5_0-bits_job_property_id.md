---
UID: NE:bits5_0.BITS_JOB_PROPERTY_ID
title: BITS_JOB_PROPERTY_ID (bits5_0.h)
description: Defines constants that specify the ID of the property for the BITS job.
helpviewer_keywords: ["BITS_JOB_PROPERTY_DYNAMIC_CONTENT","BITS_JOB_PROPERTY_HIGH_PERFORMANCE","BITS_JOB_PROPERTY_ID","BITS_JOB_PROPERTY_ID enumeration [BITS]","BITS_JOB_PROPERTY_ID_COST_FLAGS","BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE","BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS","BITS_JOB_PROPERTY_NOTIFICATION_CLSID","BITS_JOB_PROPERTY_ON_DEMAND_MODE","BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS","bits.bits_job_property_id","bits5_0/BITS_JOB_PROPERTY_DYNAMIC_CONTENT","bits5_0/BITS_JOB_PROPERTY_HIGH_PERFORMANCE","bits5_0/BITS_JOB_PROPERTY_ID","bits5_0/BITS_JOB_PROPERTY_ID_COST_FLAGS","bits5_0/BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE","bits5_0/BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS","bits5_0/BITS_JOB_PROPERTY_NOTIFICATION_CLSID","bits5_0/BITS_JOB_PROPERTY_ON_DEMAND_MODE","bits5_0/BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"]
old-location: bits\bits_job_property_id.htm
tech.root: Bits
ms.assetid: 4ED7419E-3435-4F12-B293-1FDC24F40D63
ms.date: 12/05/2018
ms.keywords: BITS_JOB_PROPERTY_DYNAMIC_CONTENT, BITS_JOB_PROPERTY_HIGH_PERFORMANCE, BITS_JOB_PROPERTY_ID, BITS_JOB_PROPERTY_ID enumeration [BITS], BITS_JOB_PROPERTY_ID_COST_FLAGS, BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE, BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS, BITS_JOB_PROPERTY_NOTIFICATION_CLSID, BITS_JOB_PROPERTY_ON_DEMAND_MODE, BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS, bits.bits_job_property_id, bits5_0/BITS_JOB_PROPERTY_DYNAMIC_CONTENT, bits5_0/BITS_JOB_PROPERTY_HIGH_PERFORMANCE, bits5_0/BITS_JOB_PROPERTY_ID, bits5_0/BITS_JOB_PROPERTY_ID_COST_FLAGS, bits5_0/BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE, bits5_0/BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS, bits5_0/BITS_JOB_PROPERTY_NOTIFICATION_CLSID, bits5_0/BITS_JOB_PROPERTY_ON_DEMAND_MODE, bits5_0/BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS
req.header: bits5_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BITS_JOB_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BITS_JOB_PROPERTY_ID
 - bits5_0/BITS_JOB_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits5_0.h
api_name:
 - BITS_JOB_PROPERTY_ID
---

# BITS_JOB_PROPERTY_ID enumeration


## -description

Defines constants that specify the ID of the property for the BITS job.

This enumeration is used in the <a href="/windows/desktop/api/bits5_0/ns-bits5_0-bits_job_property_value">BITS_JOB_PROPERTY_VALUE</a> union to determine the type of value contained in the union.

## -enum-fields

### -field BITS_JOB_PROPERTY_ID_COST_FLAGS:1

The ID that is used to <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_transfer_policy">control transfer behavior</a> over cellular and/or similar networks. This property may be changed while a transfer is ongoing – the new cost flags will take effect immediately. 

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>'s <b>DWORD</b> field.

### -field BITS_JOB_PROPERTY_NOTIFICATION_CLSID:2

The ID that is used to <a href="/windows/desktop/Bits/registering-a-com-callback">register a COM callback</a> by CLSID to receive notifications about the progress and completion of a BITS job. The CLSID must refer to a class associated with a registered out-of-process COM server. It may also be set to <b>GUID_NULL</b> to clear a previously set notification CLSID. 

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>CLsID</b> field.

### -field BITS_JOB_PROPERTY_DYNAMIC_CONTENT:3

The ID for marking a BITS job as being willing to download  content which does not support the normal <a href="/windows/desktop/Bits/http-requirements-for-bits-downloads">HTTP requirements for BITS downloads</a>: HEAD requests, the Content-Length header, and the Content-Range header. Downloading this type of content is opt-in, because BITS cannot pause and resume downloads jobs without that support. If a job with this property enabled is interrupted for any reason, such as a temporary loss of network connectivity or the system rebooting, BITS will restart the download from the beginning instead of resuming where it left off. BITS also cannot throttle bandwidth usage for dynamic downloads; BITS will not perform unthrottled transfers for any job that does not have <b>BG_JOB_PRIORITY_FOREGROUND</b> assigned, so you should typically set that priority every time you use set a job as allowing dynamic content. 

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>Enable</b> field. This property is only supported for <b>BG_JOB_TYPE_DOWNLOAD</b> jobs. It is not supported for downloads that use <b>FILE_RANGES</b>. This property may only be set prior to the first time <b>Resume</b> is called on a job.

### -field BITS_JOB_PROPERTY_HIGH_PERFORMANCE:4

The ID for marking a BITS job as not requiring strong reliability guarantees.  Enabling this property will cause BITS to avoid persisting information about normal job progress, which BITS normally does periodically. In the event of an unexpected shutdown, such as a power loss, during a transfer, this will cause BITS to lose progress 

and restart the job from the beginning instead of resuming from where it left off as usual. However, it will also reduce the number of disk writes BITS makes over the course of a job’s lifetime, which can improve performance for smaller jobs. 

This property also causes BITS to download directly into the destination file, instead of downloading to a temporary file and moving the temporary file to the final destination once the transfer is complete. This means that BITS will not clean up any partially downloaded content if a job is cancelled or encounters a fatal error condition; the BITS caller is responsible for cleaning up the destination file, if it gets created. However, it will also slightly reduce disk overhead.

This property is only recommended for scenarios which involve high numbers of small jobs (under 1MB) and which do not require reliability to power loss or other unexpected shutdown events. The performance savings are not generally significant for small numbers of jobs or for larger jobs.

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>Enable</b> field. This property is only supported for <b>BG_JOB_TYPE_DOWNLOAD</b> jobs. This property may only be set prior to adding any files to a job.

### -field BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE:5

The ID for marking the maximum number of bytes a BITS job will be allowed to download in total. This property is intended for use with <b>BITS_JOB_PROPERTY_DYNAMIC_CONTENT</b>, where you may not be able to determine the size of the file to be downloaded ahead of time but would like to cap the total possible download size.

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>Enable</b> field. This property is only supported for <b>BG_JOB_TYPE_DOWNLOAD</b> jobs. This property may only be set prior to the first time <b>Resume</b> is called on a job.

### -field BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS:7

The ID for marking a BITS job as being willing to include default credentials in requests to proxy servers. Enabling this property is equivalent to setting a <a href="/windows/desktop/WinHttp/authentication-in-winhttp">WinHTTP security level</a> of <b>WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM</b> on the requests that BITS makes on the user’s behalf. The user BITS retrieves stored credentials from the is the same as the one it makes network requests on behalf of: BITS will normally use the job owner’s credentials, unless you have explicitly provided a network <a href="/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs">helper token</a>, in which case BITS will use the network helper token’s credentials.

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>Target</b> field. However, only the <b>BG_AUTH_TARGET_PROXY</b> target is supported.

### -field BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS:9

The ID that is used to control the timing of BITS JobNotification and <a href="/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred">FileRangesTransferred</a> notifications.  Enabling this property lets a user be notified at a different rate.  This property may be changed while a transfer is ongoing; however, the new rate may not be applied immediately.  The default value is 500 milliseconds.

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>’s <b>DWORD</b> field.

### -field BITS_JOB_PROPERTY_ON_DEMAND_MODE:10

The ID that is used to control whether a job is in On Demand mode. On Demand jobs allow the app to request particular ranges for a file download instead of downloading from the start to the end. The default value is <b>FALSE</b>; the job is not on-demand. Ranges are requested using the <a href="/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges">IBackgroundCopyFile6::RequestFileRanges</a> method.

This property uses the <b>BITS_JOB_PROPERTY_VALUE</b>'s <b>Enable</b> field.   

The requirements for a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job is that the transfer must be a  <b>BG_JOB_TYPE_DOWNLOAD</b>  job.  The job must not be <b>DYNAMIC</b> and the server must be an HTTP or HTTPS server and the server requirements for range support must all be met.

## -see-also

* <a href="/windows/desktop/api/bits5_0/ns-bits5_0-bits_job_property_value">BITS_JOB_PROPERTY_VALUE</a>
* <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_transfer_policy">BITS_JOB_TRANSFER_POLICY</a>
* <a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyjob5-getproperty">IBackgroundCopyJob5::GetProperty</a>
* <a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty">IBackgroundCopyJob5::SetProperty</a>
