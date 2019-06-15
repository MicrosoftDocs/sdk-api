---
UID: NF:resapi.ResUtilVerifyPrivatePropertyList
title: ResUtilVerifyPrivatePropertyList function (resapi.h)
author: windows-sdk-content
description: Verifies that a property list is correctly formatted.
old-location: mscs\resutilverifyprivatepropertylist.htm
tech.root: MsCS
ms.assetid: 3d2eaa83-dd82-4023-8466-0131f7b90abc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST, PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST function [Failover Cluster], ResUtilVerifyPrivatePropertyList, ResUtilVerifyPrivatePropertyList function [Failover Cluster], _wolf_resutilverifyprivatepropertylist, mscs.resutilverifyprivatepropertylist, resapi/PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST, resapi/ResUtilVerifyPrivatePropertyList
ms.topic: function
f1_keywords: ["resapi/ResUtilVerifyPrivatePropertyList"]
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilVerifyPrivatePropertyList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilVerifyPrivatePropertyList function


## -description


Verifies that a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/property-lists">property list</a> is correctly formatted.


## -parameters




### -param pInPropertyList [in]

Pointer to an input buffer containing the property list to verify.


### -param cbInPropertyListSize [in]

Size of the input buffer pointed to by <i>pInPropertyList</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilsetprivatepropertylist">ResUtilSetPrivatePropertyList</a>
 

 

