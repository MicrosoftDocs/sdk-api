---
UID: NF:wtsprotocol.IWRdsWddmIddProps.GetHardwareId
title: IWRdsWddmIddProps::GetHardwareId (wtsprotocol.h)
description: Protocol stack uses this method to return hardware Id of WDDM ID driver.
helpviewer_keywords: ["GetHardwareId","GetHardwareId method [Remote Desktop Services]","GetHardwareId method [Remote Desktop Services]","IWRdsWddmIddProps interface","IWRdsWddmIddProps interface [Remote Desktop Services]","GetHardwareId method","IWRdsWddmIddProps.GetHardwareId","IWRdsWddmIddProps::GetHardwareId","termserv.iwrdswddmiddprops_gethardwareid","wtsprotocol/IWRdsWddmIddProps::GetHardwareId"]
old-location: termserv\iwrdswddmiddprops_gethardwareid.htm
tech.root: TermServ
ms.assetid: 4F9D2C6D-6555-4ABE-B856-6DD59B139978
ms.date: 12/05/2018
ms.keywords: GetHardwareId, GetHardwareId method [Remote Desktop Services], GetHardwareId method [Remote Desktop Services],IWRdsWddmIddProps interface, IWRdsWddmIddProps interface [Remote Desktop Services],GetHardwareId method, IWRdsWddmIddProps.GetHardwareId, IWRdsWddmIddProps::GetHardwareId, termserv.iwrdswddmiddprops_gethardwareid, wtsprotocol/IWRdsWddmIddProps::GetHardwareId
req.header: wtsprotocol.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsWddmIddProps::GetHardwareId
 - wtsprotocol/IWRdsWddmIddProps::GetHardwareId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWRdsWddmIddProps.GetHardwareId
---

# IWRdsWddmIddProps::GetHardwareId


## -description

Protocol stack uses this method to return hardware Id of WDDM ID driver.

## -parameters

### -param pDisplayDriverHardwareId [in]

Pointer to an array that contains the hardware ID.

### -param Count [in]

Size in elements of the hardware ID string.

## -returns

S_OK or error code

## -see-also

<a href="nn-wtsprotocol-iwrdswddmiddprops.md">IWRdsWddmIddProps</a>

