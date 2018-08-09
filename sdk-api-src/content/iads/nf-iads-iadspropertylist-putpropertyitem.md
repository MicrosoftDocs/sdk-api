---
UID: NF:iads.IADsPropertyList.PutPropertyItem
title: IADsPropertyList::PutPropertyItem
author: windows-sdk-content
description: Updates the values for an item in the property list.
old-location: adsi\iadspropertylist_putpropertyitem.htm
old-project: ADSI
ms.assetid: 16af5cbf-3b87-467e-8e72-0110bcf95295
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsPropertyList interface [ADSI],PutPropertyItem method, IADsPropertyList.PutPropertyItem, IADsPropertyList::PutPropertyItem, PutPropertyItem, PutPropertyItem method [ADSI], PutPropertyItem method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_putpropertyitem, adsi.iadspropertylist__putpropertyitem, adsi.iadspropertylist_putpropertyitem, iads/IADsPropertyList::PutPropertyItem
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPropertyList::PutPropertyItem


## -description


The <b>IADsPropertyList::PutPropertyItem</b> method updates the values for an item in the property list.


## -parameters




### -param varData






#### - VarData [in]

New property values to be put in the property cache. This should contain the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> pointer to the object which implements the  <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> that contain the modified property values.


## -returns



This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The  <a href="https://msdn.microsoft.com/73b0f6d4-55db-46cf-a781-e10bc4fcf2db">IADsPropertyEntry::put_ControlCode</a> should be set to the desired modify / add / delete operation by using the proper  <a href="https://msdn.microsoft.com/fba20292-870d-4948-abf1-225b1230e938">ADS_PROPERTY_OPERATION_ENUM</a> value. After <b>PutPropertyItem</b> has been called, you must call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> to persist any changes in the directory store. The property values are not committed until the <b>IADs::SetInfo</b> method is called.


#### Examples

The following code example shows how to add a new entry to a property list using <b>PutPropertyItem</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim propList As IADsPropertyList
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
    If(Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If

    Set propList = Nothing
    Set propVal = Nothing
    Set propEntry = Nothing
    Set IADsObj = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example adds a new entry to a property list using <b>IADsPropertyList::PutPropertyItem</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// forward declaration of a helper function
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
                      (void**)&amp;pList);

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
                         (void**)&amp;pVal);
   if(hr!=S_OK)
   {
      _tprintf(TEXT("An error has occurred."));
      pList-&gt;Release();
      return;
   }

   hr = pVal-&gt;put_CaseIgnoreString(CComBSTR("Fabrikam, Inc - Seattle, WA"));

   hr = pVal-&gt;put_ADsType(ADSTYPE_CASE_IGNORE_STRING);

   // put the propertyValue object into a variant array for 
   // assignment to a propertyEntry object
   IDispatch *pDisp;
   hr = pVal-&gt;QueryInterface(IID_IDispatch,(void**)&amp;pDisp);
   hr = pVal-&gt;Release();

   VARIANT vVals;
   VariantInit(&amp;vVals);
   hr = ADsBuildVarArrayDisp(&amp;pDisp,1,&amp;vVals);  //code given below.
   pDisp-&gt;Release();  

   if(hr!=S_OK)
   {
      _tprintf(TEXT("An error has occurred."));
      pList-&gt;Release();
      return;
   }

   // Create a propertyEntry object
   IADsPropertyEntry *pEntry;
   hr = CoCreateInstance(CLSID_PropertyEntry,
                         NULL,
                         CLSCTX_INPROC_SERVER,
                         IID_IADsPropertyEntry,
                         (void**)&amp;pEntry);

   hr = pEntry-&gt;put_Name(CComBSTR("adminDescription"));
   hr = pEntry-&gt;put_ControlCode(ADS_PROPERTY_UPDATE);
   hr = pEntry-&gt;put_ADsType(ADSTYPE_CASE_IGNORE_STRING);
   hr = pEntry-&gt;put_Values(vVals);
   VariantClear(&amp;vVals);

   // Convert pEntry to pDisp for use in pList.PutPropertyItem
   hr = pEntry-&gt;QueryInterface(IID_IDispatch,(void**)&amp;pDisp);
   pEntry-&gt;Release();

   VARIANT vEntry;
   VariantInit(&amp;vEntry);
   V_DISPATCH(&amp;vEntry)=pDisp;
   V_VT(&amp;vEntry)=  VT_DISPATCH;
   hr = pList-&gt;PutPropertyItem(vEntry);  
   VariantClear(&amp;vEntry);

   IADs *pObj;
   hr = pList-&gt;QueryInterface(IID_IADs,(void**)&amp;pObj);
   pObj-&gt;SetInfo();
   pObj-&gt;Release();

   pList-&gt;Release();

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

    if((!IDispatch) || (dwObjs&lt;=0))
    {
        return E_INVALIDARG;
    }

    sabNewArray.cElements = dwObjs;
    sabNewArray.lLbound = 0;
    psa = SafeArrayCreate(VT_VARIANT, 1, &amp;sabNewArray);

    if (!pVar) {
        hr = E_ADS_BAD_PARAMETER;
        goto Fail;
    }
    VariantInit(pVar);

    if (!psa) {
        goto Fail;
    }

    for (i = 0; i &lt; dwObjs; i++) {
        VariantInit(&amp;v);
        V_VT(&amp;v) = VT_DISPATCH;
        V_DISPATCH(&amp;v) = *(ppObjs + i);
        hr = SafeArrayPutElement(psa,
                                 (long FAR *)&amp;i,
                                 &amp;v
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

