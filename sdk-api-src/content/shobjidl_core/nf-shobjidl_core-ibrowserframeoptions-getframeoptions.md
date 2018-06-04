---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBrowserFrameOptions::GetFrameOptions


## -description


Retrieves the available browser frame view options.


## -parameters




### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/e1c75a00-304f-44ca-98a0-a6c76a1ef95f">BROWSERFRAMEOPTIONS</a></b>

Specifies the options requested as a bitwise combination of one or more of the constants of enumeration type <a href="https://msdn.microsoft.com/e1c75a00-304f-44ca-98a0-a6c76a1ef95f">BROWSERFRAMEOPTIONS</a>.


### -param pdwOptions [out]

Type: <b><a href="https://msdn.microsoft.com/e1c75a00-304f-44ca-98a0-a6c76a1ef95f">BROWSERFRAMEOPTIONS</a>*</b>


          When this method returns, contains the options that the view  can enable (for example, <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> ). This value is not optional and is always equal to, or a subset of, the options specified by <i>dwMask</i>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the method succeeds, the return value is S_OK and <i>pdwOptions</i> contains the subset of available view options.  If the method fails, <i>pdwOptions</i> is set to BFO_NONE.




