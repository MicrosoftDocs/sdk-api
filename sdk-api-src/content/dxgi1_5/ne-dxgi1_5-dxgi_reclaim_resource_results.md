---
UID: NE:dxgi1_5._DXGI_RECLAIM_RESOURCE_RESULTS
title: DXGI_RECLAIM_RESOURCE_RESULTS (dxgi1_5.h)
author: windows-sdk-content
description: Specifies result flags for the ReclaimResources1 method.
old-location: direct3ddxgi\dxgi_reclaim_resource_results.htm
tech.root: direct3ddxgi
ms.assetid: AF7082A5-6280-4602-9944-EC2DFF91BBB9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXGI_RECLAIM_RESOURCE_RESULTS, DXGI_RECLAIM_RESOURCE_RESULTS enumeration [DXGI], DXGI_RECLAIM_RESOURCE_RESULT_DISCARDED, DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED, DXGI_RECLAIM_RESOURCE_RESULT_OK, direct3ddxgi.dxgi_reclaim_resource_results, dxgi1_5/DXGI_RECLAIM_RESOURCE_RESULTS, dxgi1_5/DXGI_RECLAIM_RESOURCE_RESULT_DISCARDED, dxgi1_5/DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED, dxgi1_5/DXGI_RECLAIM_RESOURCE_RESULT_OK
ms.topic: enum
req.header: dxgi1_5.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_5.h
api_name:
 - DXGI_RECLAIM_RESOURCE_RESULTS
product: Windows
targetos: Windows
req.typenames: DXGI_RECLAIM_RESOURCE_RESULTS
req.redist: 
---

# DXGI_RECLAIM_RESOURCE_RESULTS enumeration


## -description


Specifies result flags for the <a href="https://msdn.microsoft.com/83D09C41-CB96-4ADA-AE38-7D9542CCCFE0">ReclaimResources1</a> method.


## -enum-fields




### -field DXGI_RECLAIM_RESOURCE_RESULT_OK

The surface was successfully reclaimed and has valid content. This result is identical to the <i>false</i> value returned by the older <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a> API.


### -field DXGI_RECLAIM_RESOURCE_RESULT_DISCARDED

The surface was reclaimed, but the old content was lost and must be regenerated. This result is identical to the <i>true</i> value returned by the older <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a> API.


### -field DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED

 Both the surface and its contents are lost and invalid. The surface must be 
recreated and the content regenerated in order to be used. All future use of that resource is invalid. Attempts to bind it to the pipeline or map a resource which returns this value will never succeed, and the resource cannot be reclaimed again.


## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

