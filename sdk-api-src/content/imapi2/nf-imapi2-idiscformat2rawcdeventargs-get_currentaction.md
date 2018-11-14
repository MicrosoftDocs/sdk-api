---
UID: NF:imapi2.IDiscFormat2RawCDEventArgs.get_CurrentAction
title: IDiscFormat2RawCDEventArgs::get_CurrentAction
author: windows-sdk-content
description: Retrieves the current write action being performed.
old-location: imapi\idiscformat2rawcdeventargs_get_currentaction.htm
tech.root: imapi
ms.assetid: 2a29f77e-e895-4cb0-b1f0-83df07931893
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDiscFormat2RawCDEventArgs interface [IMAPI],get_CurrentAction method, IDiscFormat2RawCDEventArgs.get_CurrentAction, IDiscFormat2RawCDEventArgs::get_CurrentAction, get_CurrentAction, get_CurrentAction method [IMAPI], get_CurrentAction method [IMAPI],IDiscFormat2RawCDEventArgs interface, imapi.idiscformat2rawcdeventargs_get_currentaction, imapi2/IDiscFormat2RawCDEventArgs::get_CurrentAction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2RawCDEventArgs.get_CurrentAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IDiscFormat2RawCDEventArgs.get_CurrentAction
: 
---

# IDiscFormat2RawCDEventArgs::get_CurrentAction


## -description


Retrieves the current write action being performed.


## -parameters




### -param value [out]

Current write action being performed. For a list of possible actions, see  the <a href="https://msdn.microsoft.com/eb19b3e1-59b2-4649-87c5-057d50213ef2">IMAPI_FORMAT2_RAW_CD_WRITE_ACTION</a> enumeration type.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a06911e-8a50-4e41-874c-478ad05f6488">DDiscFormat2RawCDEvents</a>



<a href="https://msdn.microsoft.com/b1988883-459c-46f1-a0d1-df9500a000e1">IDiscFormat2RawCDEventArgs</a>
 

 

