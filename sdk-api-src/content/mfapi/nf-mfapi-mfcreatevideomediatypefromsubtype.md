---
UID: NF:mfapi.MFCreateVideoMediaTypeFromSubtype
title: MFCreateVideoMediaTypeFromSubtype function
author: windows-sdk-content
description: Creates a partial video media type with a specified subtype.
old-location: mf\mfcreatevideomediatypefromsubtype.htm
old-project: medfound
ms.assetid: 3ae58096-fe11-4cc8-9887-2e13f56a958d
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 3ae58096-fe11-4cc8-9887-2e13f56a958d, MFCreateVideoMediaTypeFromSubtype, MFCreateVideoMediaTypeFromSubtype function [Media Foundation], mf.mfcreatevideomediatypefromsubtype, mfapi/MFCreateVideoMediaTypeFromSubtype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateVideoMediaTypeFromSubtype
product: Windows
targetos: Windows
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateVideoMediaTypeFromSubtype function


## -description



          Creates a partial video media type with a specified subtype.
        


## -parameters




### -param pAMSubtype [in]


            Pointer to a GUID that specifies the subtype. See <a href="https://msdn.microsoft.com/7dfd85e6-936e-4b78-a2cb-a5d59153e1c4">Video Subtype GUIDs</a>.
          


### -param ppIVideoMediaType [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This function creates a media type and sets the major type equal to <b>MFMediaType_Video</b> and the subtype equal to the value specified in <i>pAMSubtype</i>.
      

You can get the same result with the following steps:

<ol>
<li>
            Call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>. This function returns a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface.
          </li>
<li>
            Set the <a href="https://msdn.microsoft.com/b88b5fcf-8025-4638-930d-9fc5cf0ec8a3">MF_MT_MAJOR_TYPE</a> attribute to <b>MFMediaType_Video</b>.
          </li>
<li>
            Set the <a href="https://msdn.microsoft.com/8e600943-92f1-4936-8c00-842fc7f4cb57">MF_MT_SUBTYPE</a> attribute to the subtype.
          </li>
</ol>
<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://msdn.microsoft.com/library/Ee663600(v=VS.85).aspx">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

