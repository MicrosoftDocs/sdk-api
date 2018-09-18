---
UID: NF:oleacc.IAccessible.get_accState
title: IAccessible::get_accState
author: windows-sdk-content
description: The IAccessible::get_accState method retrieves the current state of the specified object. All objects support this property.
old-location: winauto\iaccessible_iaccessible__get_accstate.htm
tech.root: WinAuto
ms.assetid: e6b7e0dd-407a-4e82-889b-31ad999a72ca
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accState method, IAccessible.get_accState, IAccessible::get_accState, _msaa_IAccessible_get_accState, get_accState, get_accState method [Windows Accessibility], get_accState method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accstate, oleacc/IAccessible::get_accState, winauto.iaccessible_iaccessible__get_accstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accState
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 and Windows 95
---

# IAccessible::get_accState


## -description


The <b>IAccessible::get_accState</b> method retrieves the current state of the specified object. All objects support this property.


## -parameters




### -param varChild

TBD


### -param pvarState [out, retval]

Type: <b>VARIANT*</b>

Address of a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a> that receives information that describes the object's state. The <b>vt</b> member is VT_I4, and the <b>lVal</b> member is one or more of the <a href="https://msdn.microsoft.com/1253d2d2-d931-4380-9ae8-f4e1fdaee817">object state constants</a>.


#### - varID [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved state information belongs to the object or of one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="https://msdn.microsoft.com/0def0349-178b-4be5-aa1d-6602dc015981">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
</table>
 




## -remarks



If predefined state values are returned, clients call <a href="https://msdn.microsoft.com/2a136883-870e-48c3-b182-1cdc64768894">GetStateText</a> to retrieve a localized string that describes the object's state.

The actual state of a child often depends on the state of its ancestors. For example, controls in an application's main window are not focusable when a modal dialog box is open, but the controls may not report this state. To verify the state information of a child object, call <b>get_accState</b> for the parent object.

<b>Note to server developers:  </b>You must use the predefined state constants.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation of this method for a custom list box that maintains its own child elements (list items), only one of which can be selected at a time. If the client requests the state of the list box itself, the method passes the call to the standard accessible object that serves the control window. For child items, different flags are returned depending on whether the item is selected or not.


```cpp

// m_pStdAccessibleObject is the standard accessible object returned by CreateAccessibleObject. 
// m_pControl is the custom control instance that returns this accessible object. 

HRESULT STDMETHODCALLTYPE AccServer::get_accState( 
    VARIANT varChild,
    VARIANT *pvarState)
{
    if (varChild.vt != VT_I4)
    {
        pvarState->vt = VT_EMPTY;
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        return m_pStdAccessibleObject->get_accState(varChild, pvarState);
    }
    else  // For list items. 
    {
        DWORD flags = STATE_SYSTEM_SELECTABLE;
        int index = (int)varChild.lVal - 1;
        if (index == m_pControl->GetSelectedIndex())
        {
            flags |= STATE_SYSTEM_SELECTED;
        }
        pvarState->vt = VT_I4;
        pvarState->lVal = flags; 
    }
    return S_OK;
};

```


<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function displays the states of the specified accessible object or a child element.


```cpp

HRESULT PrintState(IAccessible* pAcc, long childId)
{
    if (pAcc == NULL)
    {
        return E_INVALIDARG;    
    }
    VARIANT      varChild;
    varChild.vt = VT_I4;
    varChild.lVal = childId;
    VARIANT varResult;
    HRESULT hr = pAcc->get_accState(varChild, &varResult);
    long stateBits = 0;
    if ((hr == S_OK) && (varResult.vt == VT_I4))
    {
        printf("State: ");
        stateBits = (DWORD)varResult.lVal;
        for (DWORD mask = 1; mask <= 0x8000; mask <<= 1)
        {
            if (mask & stateBits)
            {

                // Get the length of the string. 
                UINT stateLength = GetStateText(mask, NULL, 0);

                // Allocate memory for the string. Add one character to 
                // the length you got in the previous call to make room 
                // for the null character. 
                LPTSTR lpszStateString = (LPTSTR)malloc(
                    (stateLength + 1) * sizeof(TCHAR));
                if (lpszStateString != NULL)
                {
                    // Get the string. 
                    GetStateText(mask, 
                        lpszStateString, stateLength + 1); 
#ifdef UNICODE
                    printf("%S\n", lpszStateString);
#else
                    printf(("%s\n", lpszStateString);
#endif
                    // Free the allocated memory
                    free(lpszStateString);
                }
                else 
                {
                    return E_OUTOFMEMORY;
                }
            }
        }
    }
    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/2a136883-870e-48c3-b182-1cdc64768894">GetStateText</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/1253d2d2-d931-4380-9ae8-f4e1fdaee817">Object State Constants</a>



<a href="https://msdn.microsoft.com/6a56070f-7913-45b2-b693-3c0a8b7fa2f4">State Property</a>



<a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>
 

 

