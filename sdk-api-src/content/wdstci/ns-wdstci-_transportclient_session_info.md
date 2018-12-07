---
UID: NS:wdstci._TRANSPORTCLIENT_SESSION_INFO
title: "_TRANSPORTCLIENT_SESSION_INFO"
author: windows-sdk-content
description: This structure is used by the PFN_WdsTransportClientSessionStartEx callback function.
old-location: wds\transportclient_session_info.htm
tech.root: wds
ms.assetid: 21c96849-e122-4c4b-9d12-9f1c24908ac2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTRANSPORTCLIENT_SESSION_INFO, PTRANSPORTCLIENT_SESSION_INFO, PTRANSPORTCLIENT_SESSION_INFO structure pointer [Windows Deployment Services], TRANSPORTCLIENT_SESSION_INFO, TRANSPORTCLIENT_SESSION_INFO structure [Windows Deployment Services], _TRANSPORTCLIENT_SESSION_INFO, wds.transportclient_session_info, wdstci/PTRANSPORTCLIENT_SESSION_INFO, wdstci/TRANSPORTCLIENT_SESSION_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdstci.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstci.h
api_name:
 - TRANSPORTCLIENT_SESSION_INFO
product: Windows
targetos: Windows
req.typenames: TRANSPORTCLIENT_SESSION_INFO, *PTRANSPORTCLIENT_SESSION_INFO
req.redist: 
---

# _TRANSPORTCLIENT_SESSION_INFO structure


## -description


This structure is used by the <a href="https://msdn.microsoft.com/36970f1b-9dbf-421f-a078-3da3bbb050e8">PFN_WdsTransportClientSessionStartEx</a> callback function.


## -struct-fields




### -field ulStructureLength

The length of this structure in bytes.


### -field ullFileSize

The size of the file, in bytes.


### -field ulBlockSize

The size of a receive block, in bytes.

