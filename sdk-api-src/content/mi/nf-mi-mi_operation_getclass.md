---
UID: NF:mi.MI_Operation_GetClass
title: MI_Operation_GetClass function
author: windows-sdk-content
description: Gets a synchronous result for a class operation.
old-location: wmi_v2\mi_operation_getclass.htm
tech.root: wmi_v2
ms.assetid: f29f5a03-2b0b-4d36-97cb-f3b38f6037b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Operation_GetClass, MI_Operation_GetClass function [Windows Management Infrastructure (MI)], mi/MI_Operation_GetClass, wmi_v2.mi_operation_getclass
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - Mi.h
api_name:
 - MI_Operation_GetClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Operation_GetClass function


## -description


Gets a synchronous result for a class operation.


## -parameters




### -param operation [in]

Operation handle returned from an instance session operation.


### -param classResult

Returned class. If the operation fails, this value may be <b>Null</b>. The returned class is valid until the next call to <b>MI_Operation_GetClass</b> or <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>. If the class needs to be stay active across these calls, then the class needs to be cloned via <a href="https://msdn.microsoft.com/a95b867c-7567-4ea4-a02c-049002de2109">MI_Class_Clone</a>.


### -param moreResults [out, optional]

Returned Boolean value indicating if more results are available. A value of <b>MI_TRUE</b> means that more results can be retrieved. This is accomplished by calling this function until <b>moreResults</b> has a value of <b>MI_FALSE</b> (even if the operation is canceled via <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>. Calling <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> before retrieving the last result where <b>moreResults</b> is set to <b>MI_FALSE</b> will cause the <b>MI_Operation_Close</b> function to stop responding.


### -param result [out, optional]

Returned value indicating the success or failure of the function call. A value of <b>MI_RESULT_OK</b> indicates success. Otherwise, the returned <b>errorMessage</b> value should be used to determine the cause of failure.


### -param errorMessage

In the case of an error, this returned value provides additional debugging information as to the cause of failure. This error message has the same lifetime as the <b>classResult</b> value.


### -param completionDetails

In the case of an error, this returned value provides additional error information - typically in the form of a CIM_Error object (or a derived class). This returned instance has the same lifetime as the <b>classResult</b> value. If this value is needs to stay active longer, then the value needs to be cloned via <a href="https://msdn.microsoft.com/9c7a4659-5bc4-4d24-89bc-9da4f2bdf107">MI_Instance_Clone</a>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function will block until a result is available. It must be called until the <b>moreResults</b> parameter is returned with a value of <b>MI_FALSE</b>. It is an error to call this function if a class callback is registered.



