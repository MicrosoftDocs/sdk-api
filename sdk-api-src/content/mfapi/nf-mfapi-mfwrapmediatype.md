---
UID: NF:mfapi.MFWrapMediaType
title: MFWrapMediaType function
author: windows-sdk-content
description: Creates a media type that wraps another media type.
old-location: mf\mfwrapmediatype.htm
old-project: medfound
ms.assetid: a3dd74bc-1f1c-40b9-a43e-d45ff621248f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFWrapMediaType, MFWrapMediaType function [Media Foundation], a3dd74bc-1f1c-40b9-a43e-d45ff621248f, mf.mfwrapmediatype, mfapi/MFWrapMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFWrapMediaType
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFWrapMediaType function


## -description


Creates a media type that wraps another media type.
        


## -parameters




### -param pOrig

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to wrap in a new media type.
          


### -param MajorType

A 
            GUID that specifies the major type for the new media type. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.
          


### -param SubType

A 
            GUID that specifies the subtype for the new media type. For possible values, see:

<ul>
<li>
<a href="https://msdn.microsoft.com/55012be5-2d61-4d38-aab7-0c42f161f555">Audio Subtypes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/122beb40-410b-4f97-a09d-3d6278846a15">Video Subtypes</a>
</li>
</ul>
Applications can define custom subtype GUIDs.


### -param ppWrap

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the new media type that wraps the original media type. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The original media type (<i>pOrig</i>) is stored in the new media type under the <a href="https://msdn.microsoft.com/3bd94523-0206-44d8-83a2-e569e4ab7815">MF_MT_WRAPPED_TYPE</a> attribute. To extract the original media type, call <a href="https://msdn.microsoft.com/2cb6a5ae-315f-4de2-8817-da9d41db14b8">MFUnwrapMediaType</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

