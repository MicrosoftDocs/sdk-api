---
UID: NF:objidl.ILockBytes.SetSize
title: ILockBytes::SetSize
author: windows-sdk-content
description: The SetSize method changes the size of the byte array.
old-location: stg\ilockbytes_setsize.htm
old-project: Stg
ms.assetid: 13b3237b-d113-4505-b397-b06916368fef
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ILockBytes interface [Structured Storage],SetSize method, ILockBytes.SetSize, ILockBytes::SetSize, SetSize, SetSize method [Structured Storage], SetSize method [Structured Storage],ILockBytes interface, _stg_ilockbytes_setsize, objidl/ILockBytes::SetSize, stg.ilockbytes_setsize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	ILockBytes.SetSize
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ILockBytes::SetSize


## -description



			The <b>SetSize</b> method changes the size of the byte array.


## -parameters




### -param cb [in]

Specifies the new size of the byte array as a number of bytes.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::SetSize</b> changes the size of the byte array. If the <i>cb</i> parameter is larger than the current byte array, the byte array is extended to the indicated size by filling the intervening space with bytes of undefined value, as does 
<a href="https://msdn.microsoft.com/a27af4e1-293d-438a-8068-87275a51fd48">ILockBytes::WriteAt</a>, if the seek pointer is past the current end-of-stream.

If the <i>cb</i> parameter is smaller than the current byte array, the byte array is truncated to the indicated size.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Callers cannot rely on STG_E_MEDIUMFULL being returned at the appropriate time because of cache buffering in the operating system or network. However, callers must be able to deal with this return code because some 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> implementations might support it.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a>



<a href="https://msdn.microsoft.com/a27af4e1-293d-438a-8068-87275a51fd48">ILockBytes::WriteAt</a>
 

 

