---
UID: NF:mfidl.IMFVideoCaptureSampleAllocator.InitializeCaptureSampleAllocator
title: IMFVideoCaptureSampleAllocator::InitializeCaptureSampleAllocator
ms.date: 11/4/2019
targetos: Windows
description: Initializes the sample allocator with parameters relevant to video capture scenarios.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoCaptureSampleAllocator::InitializeCaptureSampleAllocator
f1_keywords:
 - IMFVideoCaptureSampleAllocator::InitializeCaptureSampleAllocator
 - mfidl/IMFVideoCaptureSampleAllocator::InitializeCaptureSampleAllocator
dev_langs:
 - c++
---

## -description

Initializes the sample allocator with parameters relevant to video capture scenarios.

## -parameters

### -param cbSampleSize

A DWORD specifying the sample size in bytes. The actual sample size used by the allocator is the maximum of the size required by pMediaType and cbSampleSize.

### -param cbCaptureMetadataSize

A DWORD specifying the capture metadata size in bytes. Applies only to callers that want to include additional metadata with the captured frames. The metadata size should include the size of a [KSCAMERA_METADATA_ITEMHEADER](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader) in addition to the size of the metadata payload itself.

### -param cbAlignment

A DWORD specifying the buffer alignment size in bytes. The default and minimum alignment size is 4KB. Custom alignment sizes less than 4KB will be treated as 4KB.

### -param cMinimumSamples

A DWORD specifying the minimum number of pre-allocated samples. This method will fail if the allocator cannot pre-allocate the specified minimum number of samples.

### -param pAttributes

Optional. An [IMFAttributes](../mfobjects/nn-mfobjects-imfattributes.md) store with additional configuration attributes for the sample allocator. The supported attributes are:

- [MF_SA_BUFFERS_PER_SAMPLE](/windows/win32/medfound/mf-sa-buffers-per-sample)
- [MF_SA_D3D11_BINDFLAGS](/windows/win32/medfound/mf-sa-d3d11-bindflags)
- [MF_SA_D3D11_USAGE](/windows/win32/medfound/mf-sa-d3d11-usage)
- [MF_SA_D3D11_SHARED](/windows/win32/medfound/mf-sa-d3d11-shared)
- [MF_SA_D3D11_SHARED_WITHOUT_MUTEX](/windows/win32/medfound/mf-sa-d3d11-shared-without-mutex)

### -param pMediaType

An [IMFMediaType](../mfobjects/nn-mfobjects-imfmediatype.md) specifying the media type for which samples will be allocator. The sample allocator uses this parameter to calculate the minimum required size for the media samples.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          
| Return code | Description |
|---------------|---------------|
| S_OK | The method succeeded. |
|MF_E_INVALIDMEDIATYPE | Invalid media type. |

## -remarks

## -see-also