---
UID: NF:resapi.ResUtilFindULargeIntegerProperty
title: ResUtilFindULargeIntegerProperty function (resapi.h)
description: Gets a large integer property value from a property list. The PRESUTIL_FIND_ULARGEINTEGER_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_FIND_ULARGEINTEGER_PROPERTY","PRESUTIL_FIND_ULARGEINTEGER_PROPERTY function [Failover Cluster]","ResUtilFindULargeIntegerProperty","ResUtilFindULargeIntegerProperty function [Failover Cluster]","mscs.resutilfindulargeintegerproperty","resapi/PRESUTIL_FIND_ULARGEINTEGER_PROPERTY","resapi/ResUtilFindULargeIntegerProperty"]
old-location: mscs\resutilfindulargeintegerproperty.htm
tech.root: MsCS
ms.assetid: BA4DD6F0-07DB-4601-B8EB-E79B49F2829F
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FIND_ULARGEINTEGER_PROPERTY, PRESUTIL_FIND_ULARGEINTEGER_PROPERTY function [Failover Cluster], ResUtilFindULargeIntegerProperty, ResUtilFindULargeIntegerProperty function [Failover Cluster], mscs.resutilfindulargeintegerproperty, resapi/PRESUTIL_FIND_ULARGEINTEGER_PROPERTY, resapi/ResUtilFindULargeIntegerProperty
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilFindULargeIntegerProperty
 - resapi/ResUtilFindULargeIntegerProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilFindULargeIntegerProperty
---

# ResUtilFindULargeIntegerProperty function


## -description

Gets a large integer property value from a property list. The <b>PRESUTIL_FIND_ULARGEINTEGER_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param pPropertyList [in]

A pointer to the property list.

### -param cbPropertyListSize [in]

The size of the data in <i>pPropertyList</i>, in bytes.

### -param pszPropertyName [in]

The name of the property.

### -param plPropertyValue [out]

The value of the property.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error 
       code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/property-list-parsing-functions">Property List Parsing Functions</a>