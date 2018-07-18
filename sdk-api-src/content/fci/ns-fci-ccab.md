---
UID: NS:fci.CCAB
title: CCAB
author: windows-sdk-content
description: The CCAB structure contains cabinet information.
old-location: winprog\ccab.htm
old-project: devnotes
ms.assetid: e25cb72b-4c96-40e9-9fd5-2920e4a01d3a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PCCAB, CCAB, CCAB structure [Windows API], PCCAB, PCCAB structure pointer [Windows API], fci/CCAB, fci/PCCAB, winprog.ccab"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fci.h
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
tech.root: 
req.typenames: CCAB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fci.h
api_name:
 - CCAB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# CCAB structure


## -description


The <b>CCAB</b> structure contains cabinet information.


## -struct-fields




### -field cb

The maximum size, in bytes, of a cabinet  created by FCI.


### -field cbFolderThresh

The maximum size, in bytes, that  a folder will contain before a new folder is created.


### -field cbReserveCFHeader

 


### -field cbReserveCFFolder

The size, in bytes, of the CFFolder reserve area. Possible value range is 0-255.


### -field cbReserveCFData

The size, in bytes, of the CFData reserve area. Possible value range is 0-255.


### -field iCab

The number of created cabinets.


### -field iDisk

The maximum size, in bytes, of a cabinet  created by FCI.


### -field fFailOnIncompressible

 


### -field setID

A value that represents the association between a collection of linked cabinet files.


### -field szDisk

The name of the disk on which the cabinet is placed.


### -field szCab

The name of the cabinet.


### -field szCabPath

The full path that indicates where to create the cabinet.


#### - cbReservesCFHeader

The size, in bytes, of the CFHeader reserve area. Possible value range is 0-60,000.


## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

