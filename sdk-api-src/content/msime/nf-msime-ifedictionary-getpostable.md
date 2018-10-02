---
UID: NF:msime.IFEDictionary.GetPosTable
title: IFEDictionary::GetPosTable
author: windows-sdk-content
description: Obtains the public POS (Part of Speech) table.
old-location: intl\ifedictionary_getpostable.htm
tech.root: Intl
ms.assetid: 0453B37B-A73A-4CD8-AD09-49B9A65B9FD6
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetPosTable, GetPosTable method [Internationalization for Windows Applications], GetPosTable method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],GetPosTable method, IFEDictionary.GetPosTable, IFEDictionary::GetPosTable, intl.ifedictionary_getpostable, msime/IFEDictionary::GetPosTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msime.h
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
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.GetPosTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFEDictionary::GetPosTable


## -description


Obtains the public POS (Part of Speech) table.


## -parameters




### -param prgPosTbl [out]

Pointer to the array of <a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a> structures.


### -param pcPosTbl [out]

Pointer to the number of <a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a> structures in the returned array. Can be <b>NULL</b>.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CA6A4E71-651A-44CA-B47D-79888A36BB12">POSTBL</a>
 

 

