---
UID: NF:bcrypt.BCryptHashData
title: BCryptHashData function
author: windows-sdk-content
description: Performs a one way hash or Message Authentication Code (MAC) on a data buffer.
old-location: security\bcrypthashdata_func.htm
old-project: seccng
ms.assetid: dab89dff-dc84-4f69-8b6b-de65704b0265
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BCryptHashData, BCryptHashData function [Security], bcrypt/BCryptHashData, security.bcrypthashdata_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.redist: 
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
req.typenames: HASHALGORITHM_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptHashData
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptHashData function


## -description


The <b>BCryptHashData</b> function performs a one way hash or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) on a data buffer.


## -parameters




### -param hHash [in, out]

The handle of the hash or MAC object to use to perform the operation. This handle is obtained by calling the <a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a> function.


### -param pbInput [in]

A pointer to a buffer that contains the data to process. The <i>cbInput</i> parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.


### -param cbInput [in]

The number of bytes in the <i>pbInput</i> buffer.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The hash handle in the <i>hHash</i> parameter is not valid. After the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function has been called for a hash  handle, that handle cannot be reused.

</td>
</tr>
</table>
 




## -remarks



To combine more than one buffer into the hash or MAC, you can call this function multiple times, passing a different buffer each time. To obtain the hash or MAC value, call the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function. After the <b>BCryptFinishHash</b> function has been called for a specified  handle, that handle cannot be reused.

Depending on what processor modes a provider supports, <b>BCryptHashData</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptHashData</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a>



<a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>
 

 

