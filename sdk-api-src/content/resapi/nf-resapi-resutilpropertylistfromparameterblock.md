---
UID: NF:resapi.ResUtilPropertyListFromParameterBlock
title: ResUtilPropertyListFromParameterBlock function (resapi.h)
description: Constructs a property list from a property table and a parameter block.
helpviewer_keywords: ["PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK","PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK function [Failover Cluster]","ResUtilPropertyListFromParameterBlock","ResUtilPropertyListFromParameterBlock function [Failover Cluster]","_wolf_resutilpropertylistfromparameterblock","mscs.resutilpropertylistfromparameterblock","resapi/PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK","resapi/ResUtilPropertyListFromParameterBlock"]
old-location: mscs\resutilpropertylistfromparameterblock.htm
tech.root: MsCS
ms.assetid: 6993e279-07c7-4444-b1b9-0d25360e43e3
ms.date: 12/05/2018
ms.keywords: PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK, PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK function [Failover Cluster], ResUtilPropertyListFromParameterBlock, ResUtilPropertyListFromParameterBlock function [Failover Cluster], _wolf_resutilpropertylistfromparameterblock, mscs.resutilpropertylistfromparameterblock, resapi/PRESUTIL_PROPERTY_LIST_FROM_PARAMETER_BLOCK, resapi/ResUtilPropertyListFromParameterBlock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilPropertyListFromParameterBlock
 - resapi/ResUtilPropertyListFromParameterBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ext-ms-win-cluster-resutils-l1-1-2.dll
 - ResUtils.dll
 - Ext-MS-Win-Cluster-ResUtils-L1-1-1.dll
api_name:
 - ResUtilPropertyListFromParameterBlock
---

# ResUtilPropertyListFromParameterBlock function


## -description

Constructs a 
    <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> from a 
    <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> and a 
    <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter block</a>.

## -parameters

### -param pPropertyTable [in]

Pointer to a property table describing the properties that will be included in the resulting property list.

### -param pOutPropertyList [out, optional]

Pointer to an output buffer that receives the property list.

### -param pcbOutPropertyListSize [in, out]

Pointer to the size of the output buffer in bytes.

### -param pInParams [in]

Pointer to the parameter block in which the property values are stored.

### -param pcbBytesReturned [out]

If the function returns <b>ERROR_SUCCESS</b>, <i>pcbBytesReturned</i> points to the actual byte size of the property list pointed to by <i>pOutPropertyList</i>. If the function does not return <b>ERROR_SUCCESS</b>, <i>pcbBytesReturned</i> points to a value of zero.

### -param pcbRequired [out]

If the function returns <b>ERROR_MORE_DATA</b>, <i>pcbRequired</i> points to the byte size required to contain the property list. If the function does not return <b>ERROR_MORE_DATA</b>, <i>pcbBytesReturned</i> points to a value of zero.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
       codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The output buffer is too small to contain the resulting property list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an error allocating memory.

</td>
</tr>
</table>

## -remarks

In this function, the property table determines the order in which the properties appear in the property list, as well as the name and format of each property. The function reads the property table to determine the name and format of each property.

The parameter block provides the property values.


#### Examples

The following example defines three properties (Protocol, PortNumber, and ConnectionName). It uses the 
     <b>ResUtilPropertyListFromParameterBlock</b> function to create a property list. This 
     example uses the <a href="/previous-versions/windows/desktop/mscs/clusdocex-h">ClusDocEx.h</a> header file defined in the 
     Failover Cluster documentation.


```cpp
//////////////////////////////////////////////////////////////////////

//  Be sure to create the following file before you compile.
//  For a code listing, see "ClusDocEx.h".
    #include "ClusDocEx.h"

//////////////////////////////////////////////////////////////////////

//  This example defines three fictional properties: 
//      Protocol (DWORD)
//      PortNumber (DWORD)
//      ConnectionName (PWSTR)
//  These properties are not associated with any cluster object.
//  They are used only to demonstrate the
//  ResUtilPropertyListFromParameterBlock function.

//  Protocol property constants
    #define PROP_NAME__PROTOCOL       L"Protocol"
    typedef enum PROTOCOLS{
        PROTOCOL_NONE = 0,
        PROTOCOL_BOTH = 1,
        PROTOCOL_TCP  = 2,
        PROTOCOL_UDP  = 3
    };
    #define PROP_MIN__PROTOCOL       (PROTOCOL_NONE)
    #define PROP_MAX__PROTOCOL       (PROTOCOL_UDP)
    #define PROP_DEFAULT__PROTOCOL   (PROTOCOL_BOTH)

//  PortNumber property
    #define PROP_NAME__PORTNUMBER     L"PortNumber"
    #define PROP_MIN__PORTNUMBER      (0)
    #define PROP_MAX__PORTNUMBER      (65536)
    #define PROP_DEFAULT__PORTNUMBER  (80)

//  ConnectionName property
    #define PROP_NAME__CONNECTIONNAME L"ConnectionName"

//  Parameter block
    typedef struct _PARAMBLOCK{
        DWORD dwProtocol;
        DWORD dwPortNumber;
        PWSTR pszConnectionName;
    } PARAMBLOCK; 
    
//  Property table
    RESUTIL_PROPERTY_ITEM
    pPropTable[] =
    {
        {   PROP_NAME__PROTOCOL, 
            NULL, 
            CLUSPROP_FORMAT_DWORD, 
            PROP_DEFAULT__PROTOCOL, 
            PROP_MIN__PROTOCOL, 
            PROP_MAX__PROTOCOL, 
            RESUTIL_PROPITEM_REQUIRED,  
            FIELD_OFFSET( _PARAMBLOCK, dwProtocol )        },

        {   PROP_NAME__PORTNUMBER,
            NULL, 
            CLUSPROP_FORMAT_DWORD, 
            PROP_DEFAULT__PORTNUMBER, 
            PROP_MIN__PORTNUMBER, 
            PROP_MAX__PORTNUMBER, 
            RESUTIL_PROPITEM_REQUIRED, 
            FIELD_OFFSET( _PARAMBLOCK, dwPortNumber )      },

        {   PROP_NAME__CONNECTIONNAME, 
            NULL, 
            CLUSPROP_FORMAT_SZ, 
                0, 0, 0, 0,
            FIELD_OFFSET( _PARAMBLOCK, pszConnectionName ) },

        { 0 }
    };

    int main()
    {
        DWORD nResult    = ERROR_SUCCESS,
              cbBufSize  = 1024,
              cbReturned = 0,
              cbRequired = 0;

        PVOID pPropList = LocalAlloc( LPTR, cbBufSize );

    //  Values for the property list
        PARAMBLOCK NewParams = { PROTOCOL_TCP, 21, L"FTP" };

        nResult = ResUtilPropertyListFromParameterBlock(
                      pPropTable,
                      pPropList,
                      &cbBufSize,
                      (LPBYTE) &NewParams,
                      &cbReturned,
                      &cbRequired );

        if( nResult == ERROR_MORE_DATA )
        {
            LocalFree( pPropList );

            cbBufSize = cbRequired;
            
            pPropList = LocalAlloc( LPTR, cbBufSize );

            nResult = ResUtilPropertyListFromParameterBlock(
                          pPropTable,
                          pPropList,
                          &cbBufSize,
                          (PBYTE) &NewParams,
                          &cbReturned,
                          &cbRequired );
        }

        ClusDocEx_DebugPrint( L"Results:", nResult );

        if( nResult == ERROR_SUCCESS )
            ClusDocEx_ShowBuffer( pPropList, cbReturned );    
    
        LocalFree( pPropList );
    
        return (int)( nResult != ERROR_SUCCESS );    
    }

```

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>