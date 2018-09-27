---
UID: NF:callobj.ICallIndirect.GetMethodInfo
title: ICallIndirect::GetMethodInfo
author: windows-sdk-content
description: Retrieves information about the interface method from the call frame.
old-location: com\icallindirect_getmethodinfo.htm
tech.root: com
ms.assetid: 1bfbbb24-0cdb-467b-abce-0291dfe8f641
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMethodInfo, GetMethodInfo method [COM], GetMethodInfo method [COM],ICallIndirect interface, ICallIndirect interface [COM],GetMethodInfo method, ICallIndirect.GetMethodInfo, ICallIndirect::GetMethodInfo, _com_icallindirect_getmethodinfo, callobj/ICallIndirect::GetMethodInfo, com.icallindirect_getmethodinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - Callobj.h
api_name:
 - ICallIndirect.GetMethodInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallIndirect::GetMethodInfo


## -description


Retrieves information about the interface method from the call frame.


## -parameters




### -param iMethod [in]

The method number.


### -param pInfo [out]

A pointer to the <a href="https://msdn.microsoft.com/3d490c8b-d254-458b-b355-39c3942ddc5e">CALLFRAMEINFO</a> structure containing information about the specified method.


### -param pwszMethod [out]

The method name. This parameter is optional.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



The information returned is a static analysis of the method, not a dynamic one, in that it is based on an analysis of the method signature only, not the actual current contents of the call frame. For example, the static analysis might indicate that this method has the potential of having an in-interface, but because of, say, a union switch, a given call might not actually have any such interfaces. This method is equivalent to the <a href="https://msdn.microsoft.com/807b4542-c18d-48e4-8493-c40a85e5e1de">GetInfo</a> and <a href="https://msdn.microsoft.com/3efb0819-51db-419b-a9f1-710bb3abae2d">GetNames</a> methods in <a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>, but avoids the need to actually make any invocation to get the information.




## -see-also




<a href="https://msdn.microsoft.com/b85585fd-5f44-4c07-91a4-145eb44a6bdd">ICallIndirect</a>
 

 

