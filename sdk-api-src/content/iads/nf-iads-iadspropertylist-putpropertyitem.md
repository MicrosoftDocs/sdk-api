---
UID: NF:iads.IADsPropertyList.PutPropertyItem
title: IADsPropertyList::PutPropertyItem
author: windows-sdk-content
description: Updates the values for an item in the property list.
old-location: adsi\iadspropertylist_putpropertyitem.htm
tech.root: adsi
ms.assetid: 16af5cbf-3b87-467e-8e72-0110bcf95295
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsPropertyList interface [ADSI],PutPropertyItem method, IADsPropertyList.PutPropertyItem, IADsPropertyList::PutPropertyItem, PutPropertyItem, PutPropertyItem method [ADSI], PutPropertyItem method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_putpropertyitem, adsi.iadspropertylist__putpropertyitem, adsi.iadspropertylist_putpropertyitem, iads/IADsPropertyList::PutPropertyItem
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPropertyList.PutPropertyItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsPropertyList::PutPropertyItem


## -description


The <b>IADsPropertyList::PutPropertyItem</b> method updates the values for an item in the property list.


## -parameters




### -param varData [in]

New property values to be put in the property cache. This should contain the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> pointer to the object which implements the  <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> that contain the modified property values.


## -returns



This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The  <a href="https://msdn.microsoft.com/73b0f6d4-55db-46cf-a781-e10bc4fcf2db">IADsPropertyEntry::put_ControlCode</a> should be set to the desired modify / add / delete operation by using the proper  <a href="https://msdn.microsoft.com/fba20292-870d-4948-abf1-225b1230e938">ADS_PROPERTY_OPERATION_ENUM</a> value. After <b>PutPropertyItem</b> has been called, you must call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> to persist any changes in the directory store. The property values are not committed until the <b>IADs::SetInfo</b> method is called.


#### Examples

The following code example shows how to add a new entry to a property list using <b>PutPropertyItem</b>.


```vb
Dim propList As IADsPropertyList
Dim propVal As IADsPropertyValue
Dim propEntry As IADsPropertyEntry
On Error GoTo Cleanup

Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
'--- Property Value-----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'--- Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
' --- Property List----
propList.PutPropertyItem (propEntry)
 
' query the IADs interface on the propList object
Dim IADsObj As IADs
Set IADsObj=propList
 
' Commit changes of the property list to the directory store.
IADsObj.SetInfo

Cleanup:
    If(Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
    Set propVal = Nothing
    Set propEntry = Nothing
    Set IADsObj = Nothing
```


The following code example adds a new entry to a property list using <b>IADsPropertyList::PutPropertyItem</b>.


```cpp
// forward declaration of a helper function
HRESULT ADsBuildVarArrayDisp(IDispatch ** ppObjs,
                             DWORD      dwObjs,
                             VARIANT * pVar
                             )

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsPropertyList *pList;
   hr = ADsOpenObject(L"LDAP://dc=Fabrikam,dc=com",
                      L"Administrator",
                      L"",
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsPropertyList,
                      (void**)&pList);

   if(hr!=S_OK)
   {
      _tprintf(TEXT("An error has occurred."));
      return;
   }

// create a property value object
   IADsPropertyValue *pVal;
   hr = CoCreateInstance(CLSID_PropertyValue,
                         NULL,
                         CLSCTX_INPROC_SERVER,
                         IID_IADsPropertyValue,
                         (void**)&pVal);
   if(hr!=S_OK)
   {
      _tprintf(TEXT("An error has occurred."));
      pList->Release();
      return;
   }

   hr = pVal->put_CaseIgnoreString(CComBSTR("Fabrikam, Inc - Seattle, WA"));

   hr = pVal->put_ADsType(ADSTYPE_CASE_IGNORE_STRING);

   // put the propertyValue object into a variant array for 
   // assignment to a propertyEntry object
   IDispatch *pDisp;
   hr = pVal->QueryInterface(IID_IDispatch,(void**)&pDisp);
   hr = pVal->Release();

   VARIANT vVals;
   VariantInit(&vVals);
   hr = ADsBuildVarArrayDisp(&pDisp,1,&vVals);  //code given below.
   pDisp->Release();  

   if(hr!=S_OK)
   {
      _tprintf(TEXT("An error has occurred."));
      pList->Release();
      return;
   }

   // Create a propertyEntry object
   IADsPropertyEntry *pEntry;
   hr = CoCreateInstance(CLSID_PropertyEntry,
                         NULL,
                         CLSCTX_INPROC_SERVER,
                         IID_IADsPropertyEntry,
                         (void**)&pEntry);

   hr = pEntry->put_Name(CComBSTR("adminDescription"));
   hr = pEntry->put_ControlCode(ADS_PROPERTY_UPDATE);
   hr = pEntry->put_ADsType(ADSTYPE_CASE_IGNORE_STRING);
   hr = pEntry->put_Values(vVals);
   VariantClear(&vVals);

   // Convert pEntry to pDisp for use in pList.PutPropertyItem
   hr = pEntry->QueryInterface(IID_IDispatch,(void**)&pDisp);
   pEntry->Release();

   VARIANT vEntry;
   VariantInit(&vEntry);
   V_DISPATCH(&vEntry)=pDisp;
   V_VT(&vEntry)=  VT_DISPATCH;
   hr = pList->PutPropertyItem(vEntry);  
   VariantClear(&vEntry);

   IADs *pObj;
   hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
   pObj->SetInfo();
   pObj->Release();

   pList->Release();

   CoUninitialize();
   return 0;
}

////////////////
// Helper function to build a variant array of IDispatch objects.
///////////////
HRESULT ADsBuildVarArrayDisp(
    IDispatch ** ppObjs,
    DWORD      dwObjs,
    VARIANT * pVar
    )
{

    VARIANT v;
    SAFEARRAYBOUND sabNewArray;
    DWORD i;
    SAFEARRAY *psa = NULL;
    HRESULT hr = E_FAIL;

    if((!IDispatch) || (dwObjs<=0))
    {
        return E_INVALIDARG;
    }

    sabNewArray.cElements = dwObjs;
    sabNewArray.lLbound = 0;
    psa = SafeArrayCreate(VT_VARIANT, 1, &sabNewArray);

    if (!pVar) {
        hr = E_ADS_BAD_PARAMETER;
        goto Fail;
    }
    VariantInit(pVar);

    if (!psa) {
        goto Fail;
    }

    for (i = 0; i < dwObjs; i++) {
        VariantInit(&v);
        V_VT(&v) = VT_DISPATCH;
        V_DISPATCH(&v) = *(ppObjs + i);
        hr = SafeArrayPutElement(psa,
                                 (long FAR *)&i,
                                 &v
                                 );
        if (FAILED(hr))  {
            goto Fail;
        }
    }

    V_VT(pVar) = VT_VARIANT | VT_ARRAY;
    V_ARRAY(pVar) = psa;

    return(ResultFromScode(S_OK));

Fail:
    if (psa) {
        SafeArrayDestroy(psa);
    }

    return(E_FAIL);
}
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

