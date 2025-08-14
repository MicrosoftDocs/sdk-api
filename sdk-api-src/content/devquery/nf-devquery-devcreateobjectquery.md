---
UID: NF:devquery.DevCreateObjectQuery
tech.root: devinst
title: DevCreateObjectQuery
ms.date: 11/05/2024
targetos: Windows
description: Creates a device query to retrieve properties based on the specified query parameters.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Cfgmgr32.dll
req.header: devquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1809
req.target-min-winversvr: Windows Server 2019
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-query-l1-1-1.dll
 - api-ms-win-devices-query-l1-1-0.dll
 - Cfgmgr32.dll
api_name:
 - DevCreateObjectQuery
f1_keywords:
 - DevCreateObjectQuery
 - devquery/DevCreateObjectQuery
dev_langs:
 - c++
helpviewer_keywords:
 - DevCreateObjectQuery
---

## -description

Creates a device query to retrieve properties based on the specified query parameters.

## -parameters

### -param ObjectType [in]

A value from the [DEV_OBJECT_TYPE](../devquerydef/ne-devquerydef-dev_object_type.md) enumeration that determines the object type that this query should operate on.

### -param QueryFlags [in]

A combination of [DEV_QUERY_FLAGS](../devquerydef/ne-devquerydef-dev_query_flags.md) values that are combined by using a bitwise OR operation.

### -param cRequestedProperties [in]

The number of [DEVPROPCOMPKEY](/windows-hardware/drivers/install/devpropcompkey) structures provided in *pRequestedProperties*. If [DevQueryFlagAllProperties](../devquerydef/ne-devquerydef-dev_query_flags.md) is specified, this must be set to 0.

### -param pRequestedProperties [in]

Optionally provides an array of **DEVPROPCOMPKEY** structures that specify the properties that should be retrieved for objects in the
query’s result set when *pCallback* is called to notify the query of an addition of an object to its result set.  
If [DevQueryFlagUpdateResults](../devquerydef/ne-devquerydef-dev_query_flags.md) was specified in *QueryFlags*, the query will be notified
if the value of any of these properties changes for any object in the query’s result set.

The *LocaleName* field of the **DEVPROPCOMPKEY** structure is ignored and must be set to NULL.

If *cRequestedProperties* is 0, this must be NULL.

### -param cFilterExpressionCount [in]

The number of [DEVPROP_FILTER_EXPRESSION](../devfiltertypes/ns-devfiltertypes-devprop_filter_expression.md) structures provided in *pFilter*.

### -param pFilter [in, optional]

Optionally provides an array of **DEVPROP_FILTER_EXPRESSION** structures that specify filter criteria for what objects should be part
of the query’s result set. If *cFilterExpressionCount* is 0, this must be NULL.

### -param pCallback [in]

A [PDEV_QUERY_RESULT_CALLBACK](nc-devquery-pdev_query_result_callback.md) callback function that results for this query should be sent to.

### -param pContext [in, optional]

Caller-supplied context. This value is passed to the callback function unmodified.

### -param phDevQuery [out]

Pointer that receives the handle representing the query. If **DevQueryFlagsUpdateResults** is specified, then the query will receive
updates until the handle is closed. Call [DevCloseObjectQuery](nf-devquery-devcloseobjectquery.md) to close this handle to stop the query.

## -returns

S_OK is returned if a query was successfully created; otherwise, an appropriate error value.

## -remarks

Use the **DevCreateObjectQuery** to query data about the specified **DEV_OBJECT_TYPE**. Objects are represented by an object type, a string
identity, and a property store of key / value pairs. Each query has a result-set associated with it. Objects are added, updated, or removed
from the result-set based on system state and changes and the associated callback function is notified. Each call into the callback function
represents a snapshot of the property values at the time that the callback is invoked. Only objects that match the criteria expressed in the
*pFilter* expression are returned to the caller. In addition to callback invocations that update the result-set, there are also state-change
callbacks that notify the client of changes to the state of the query.

By default, queries do not receive updates after the current state of the system has been processed. Once all matching objects have been added to the result-set, the query enters the [DevQueryStateEnumCompleted](../devquerydef/ne-devquerydef-dev_query_state.md) state and no further callbacks
will be made. When a query registers for updates by specifying the **DevQueryFlagUpdateResults** flag, its result-set will continue to be
updated, and associated callback notified, after the query enters the **DevQueryStateEnumCompleted** state as changes in the system occur that
add or remove objects based on the filter expression matching.

A query may be aborted. This happens when an internal error happens that makes it impossible to communicate a notification to the client. For example, this can happen when the system is in an out-of-memory condition. When this happens, the caller’s result-set no longer reflects a true representation of the state of the query. The caller will receive a [DevQueryStateAborted](../devquerydef/ne-devquerydef-dev_query_state.md) callback. No further callbacks will be received. The caller must close the query and create a new query to recover from this condition.

## Examples

In the following example, the **PDEV_QUERY_RESULT_CALLBACK** method is implemented to print out status messages when the query state changes, when items have
been added to, updated, or removed from the query result. Next, a simple query scenario is implemented where **DevCreateObjectQuery** is called with
a **DEVPROPCOMPKEY** array and a **DEVPROP_FILTER_EXPRESSION** to query for **DevObjectTypeDevice** objects with a **DEVPKEY_Device_ClassGuid** property with a value of **GUID_DEVCLASS_NET**.

```cpp
void WINAPI
Example1Callback(
    HDEVQUERY hDevQuery,
    PVOID pContext,
    const DEV_QUERY_RESULT_ACTION_DATA *pActionData
    )
{
    const DEVPROPERTY* NameProperty = NULL;

    UNREFERENCED_PARAMETER(hDevQuery);
    UNREFERENCED_PARAMETER(pContext);

    switch (pActionData->Action)
    {
    case DevQueryResultStateChange:
        if (pActionData->Data.State == DevQueryStateEnumCompleted)
        {
            wprintf(L"Enumeration of current system state complete.\n");
        }
        else if (pActionData->Data.State == DevQueryStateAborted)
        {
            wprintf(L"Query has aborted. No further results will be received.\n");
            // Communicate back to the creator of the query that it has aborted
            // so it can handle that appropriately, such as by recreating the
            // query
        }
        break;

    case DevQueryResultAdd:
        wprintf(L"Object '%ws' has been added to the result set.\n",
                pActionData->Data.DeviceObject.pszObjectId);

        NameProperty = DevFindProperty(&DEVPKEY_NAME,
                                       DEVPROP_STORE_SYSTEM,
                                       NULL,
                                       pActionData->Data.DeviceObject.cPropertyCount,
                                       pActionData->Data.DeviceObject.pProperties);

        if ((NameProperty == NULL) ||
            (NameProperty->Type == DEVPROP_TYPE_EMPTY) ||
            (NameProperty->Buffer == NULL))
        {
            wprintf(L"Object '%ws' had no name property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else if ((NameProperty->Type != DEVPROP_TYPE_STRING) ||
                 (NameProperty->BufferSize < sizeof(WCHAR)))
        {
            wprintf(L"Object '%ws' had a corrupted name property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else
        {
            wprintf(L"Object '%ws' has name '%ws'.\n",
                    pActionData->Data.DeviceObject.pszObjectId,
                    (PWSTR)NameProperty->Buffer);
        }

        break;

    case DevQueryResultUpdate:
        wprintf(L"Object '%ws' was updated.\n",
                pActionData->Data.DeviceObject.pszObjectId);

        NameProperty = DevFindProperty(&DEVPKEY_NAME,
                                       DEVPROP_STORE_SYSTEM,
                                       NULL,
                                       pActionData->Data.DeviceObject.cPropertyCount,
                                       pActionData->Data.DeviceObject.pProperties);

        if ((NameProperty == NULL) ||
            (NameProperty->Type == DEVPROP_TYPE_EMPTY) ||
            (NameProperty->Buffer == NULL))
        {
            wprintf(L"Object '%ws' had no name property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else if ((NameProperty->Type != DEVPROP_TYPE_STRING) ||
                 (NameProperty->BufferSize < sizeof(WCHAR)))
        {
            wprintf(L"Object '%ws' had a corrupted name property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else
        {
            wprintf(L"Object '%ws' has name '%ws'.\n",
                    pActionData->Data.DeviceObject.pszObjectId,
                    (PWSTR)NameProperty->Buffer);
        }

        break;

    case DevQueryResultRemove:
        wprintf(L"Object '%ws' has been removed from the result set.\n",
                pActionData->Data.DeviceObject.pszObjectId);
        break;
    }
}

void
Example1()
{
    DEVPROPCOMPKEY RequestedProperties[] =
    {
        { DEVPKEY_NAME, DEVPROP_STORE_SYSTEM, NULL }
    };
    DEVPROP_FILTER_EXPRESSION ObjectFilter[] =
    {
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_Device_ClassGuid, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_GUID,
                sizeof(GUID),
                (void*)&GUID_DEVCLASS_NET
            }
        }
    };

    HDEVQUERY hDevQuery = NULL;
    HRESULT hr = DevCreateObjectQuery(DevObjectTypeDevice,
                                      DevQueryFlagUpdateResults,
                                      RTL_NUMBER_OF(RequestedProperties),
                                      RequestedProperties,
                                      RTL_NUMBER_OF(ObjectFilter),
                                      ObjectFilter,
                                      Example1Callback,
                                      NULL,
                                      &hDevQuery);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create query. hr = 0x%08x\n", hr);
        goto exit;
    }

    // do other work while the query monitors system state in the background

  exit:

    if (hDevQuery != NULL)
    {
        DevCloseObjectQuery(hDevQuery);
    }

    return;
}

```

In the following example, the optional caller-defined *pContext* parameter is used to pass an event handle into the **PDEV_QUERY_RESULT_CALLBACK**
method. When the callback detects that the query state is **DevQueryStateAborted**, the event is signaled to notify the caller that it should dispose
of the existing query and recreate a new query.

```cpp
typedef struct _MY_QUERY_CONTEXT {
    HANDLE CompletionEvent;
    HRESULT hr;
} MY_QUERY_CONTEXT, *PMY_QUERY_CONTEXT;

void WINAPI
Example2Callback(
    HDEVQUERY hDevQuery,
    PVOID pContext,
    const DEV_QUERY_RESULT_ACTION_DATA *pActionData
    )
{
    PMY_QUERY_CONTEXT QueryContext = (PMY_QUERY_CONTEXT)pContext;
    const DEVPROPERTY* DevProperty = NULL;

    UNREFERENCED_PARAMETER(hDevQuery);

    switch (pActionData->Action)
    {
    case DevQueryResultStateChange:
        if (pActionData->Data.State == DevQueryStateEnumCompleted)
        {
            wprintf(L"Enumeration of current system state complete.\n");
            // The query did not use DevQueryFlagUpdateResults so the result set
            // is now complete. Signal the caller to stop waiting.
            if (!SetEvent(QueryContext->CompletionEvent))
            {
                wprintf(L"Failed to signal completion event. Err = 0x%08x\n",
                        GetLastError());
            }
        }
        else if (pActionData->Data.State == DevQueryStateAborted)
        {
            wprintf(L"Query has aborted. No further results will be received.\n");
            QueryContext->hr = E_FAIL;
            // Communicate back to the creator of the query that it has aborted
            // so it can handle that appropriately, such as by recreating the
            // query.
            if (!SetEvent(QueryContext->CompletionEvent))
            {
                wprintf(L"Failed to signal completion event. Err = 0x%08x\n",
                        GetLastError());
            }
        }
        break;

    case DevQueryResultAdd:
        wprintf(L"Object '%ws' has been added to the result set.\n",
                pActionData->Data.DeviceObject.pszObjectId);

        DevProperty = DevFindProperty(&DEVPKEY_Device_InstanceId,
                                      DEVPROP_STORE_SYSTEM,
                                      NULL,
                                      pActionData->Data.DeviceObject.cPropertyCount,
                                      pActionData->Data.DeviceObject.pProperties);

        if ((DevProperty == NULL) ||
            (DevProperty->Type == DEVPROP_TYPE_EMPTY) ||
            (DevProperty->Buffer == NULL))
        {
            wprintf(L"Object '%ws' had no instance ID property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else if ((DevProperty->Type != DEVPROP_TYPE_STRING) ||
                 (DevProperty->BufferSize < sizeof(WCHAR)))
        {
            wprintf(L"Object '%ws' had a corrupted instance ID property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else
        {
            wprintf(L"Object '%ws' was exposed by instance ID '%ws'.\n",
                    pActionData->Data.DeviceObject.pszObjectId,
                    (PWSTR)DevProperty->Buffer);
        }

        break;

    case DevQueryResultUpdate:
        wprintf(L"Object '%ws' was updated.\n",
                pActionData->Data.DeviceObject.pszObjectId);

        DevProperty = DevFindProperty(&DEVPKEY_Device_InstanceId,
                                      DEVPROP_STORE_SYSTEM,
                                      NULL,
                                      pActionData->Data.DeviceObject.cPropertyCount,
                                      pActionData->Data.DeviceObject.pProperties);

        if ((DevProperty == NULL) ||
            (DevProperty->Type == DEVPROP_TYPE_EMPTY) ||
            (DevProperty->Buffer == NULL))
        {
            wprintf(L"Object '%ws' had no instance ID property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else if ((DevProperty->Type != DEVPROP_TYPE_STRING) ||
                 (DevProperty->BufferSize < sizeof(WCHAR)))
        {
            wprintf(L"Object '%ws' had a corrupted instance ID property.\n",
                    pActionData->Data.DeviceObject.pszObjectId);
        }
        else
        {
            wprintf(L"Object '%ws' was exposed by instance ID '%ws'.\n",
                    pActionData->Data.DeviceObject.pszObjectId,
                    (PWSTR)DevProperty->Buffer);
        }

        break;

    case DevQueryResultRemove:
        wprintf(L"Object '%ws' has been removed from the result set.\n",
                pActionData->Data.DeviceObject.pszObjectId);
        break;
    }
}

void
Example2()
{
    HRESULT hr = S_OK;
    MY_QUERY_CONTEXT QueryContext = {0};
    HDEVQUERY hDevQuery = NULL;
    DEVPROP_BOOLEAN DevPropTrue = DEVPROP_TRUE;
    DEVPROPCOMPKEY RequestedProperties[] =
    {
        { DEVPKEY_Device_InstanceId, DEVPROP_STORE_SYSTEM, NULL }
    };
    DEVPROP_FILTER_EXPRESSION ObjectFilter[] =
    {
        {
            DEVPROP_OPERATOR_AND_OPEN, {0}
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_Enabled, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_BOOLEAN,
                sizeof(DevPropTrue),
                (void*)&DevPropTrue
            }
        },
        {
            DEVPROP_OPERATOR_OR_OPEN, {0}
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_ClassGuid, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_GUID,
                sizeof(GUID),
                (void*)&GUID_DEVINTERFACE_MOUSE
            }
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_ClassGuid, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_GUID,
                sizeof(GUID),
                (void*)&GUID_DEVINTERFACE_KEYBOARD
            }
        },
        {
            DEVPROP_OPERATOR_OR_CLOSE, {0}
        },
        {
            DEVPROP_OPERATOR_AND_CLOSE, {0}
        }
    };

    QueryContext.CompletionEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (!QueryContext.CompletionEvent)
    {
        wprintf(L"Failed to create event. Error = 0x%08x\n",
                GetLastError());
        goto exit;
    }

    hr = DevCreateObjectQuery(DevObjectTypeDeviceInterface,
                              DevQueryFlagNone,
                              RTL_NUMBER_OF(RequestedProperties),
                              RequestedProperties,
                              RTL_NUMBER_OF(ObjectFilter),
                              ObjectFilter,
                              Example2Callback,
                              &QueryContext,
                              &hDevQuery);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create query. hr = 0x%08x\n", hr);
        goto exit;
    }

    switch (WaitForSingleObject(QueryContext.CompletionEvent, INFINITE))
    {
    case WAIT_OBJECT_0:
        if (SUCCEEDED(QueryContext.hr))
        {
            wprintf(L"Successfully enumerated results.\n");
        }
        else
        {
            wprintf(L"Failed to Successfully enumerate results. hr = 0x%08x\n",
                    QueryContext.hr);
        }
        break;

    default:
        wprintf(L"An error waiting occurred.\n");
        break;
    }

  exit:

    if (hDevQuery != NULL)
    {
        DevCloseObjectQuery(hDevQuery);
    }

    if (QueryContext.CompletionEvent != NULL)
    {
        CloseHandle(QueryContext.CompletionEvent);
    }

    return;
}

```


## -see-also

[DevCreateObjectQueryEx](nf-devquery-devcreateobjectqueryex.md)