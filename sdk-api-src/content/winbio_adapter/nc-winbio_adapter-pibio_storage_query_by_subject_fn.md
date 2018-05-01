---
UID: NC:winbio_adapter.PIBIO_STORAGE_QUERY_BY_SUBJECT_FN
title: PIBIO_STORAGE_QUERY_BY_SUBJECT_FN
author: windows-driver-content
description: Queries the database that is currently open for templates associated with a specified identity and sub-factor.
old-location: secbiomet\storageadapterquerybysubject.htm
old-project: SecBioMet
ms.assetid: b2c93122-fae1-44ad-97d4-f90115194a31
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PIBIO_STORAGE_QUERY_BY_SUBJECT_FN, StorageAdapterQueryBySubject, StorageAdapterQueryBySubject callback function [Windows Biometric Framework API], secbiomet.storageadapterquerybysubject, winbio_adapter/StorageAdapterQueryBySubject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	StorageAdapterQueryBySubject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_QUERY_BY_SUBJECT_FN callback


## -description


Called by the Windows Biometric Framework or by the engine adapter to locate templates that match a specified identity and sub-factor.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param Identity [in]

Pointer to a  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the GUID or SID to be located. If the <b>Type</b> field of this structure contains <b>WINBIO_IDENTITY_TYPE_WILDCARD</b>, the query returns every template that matches the <i>SubFactor</i> parameter.




### -param SubFactor [in]

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the sub-factor to be located. If this value is <b>WINBIO_SUBTYPE_ANY</b>, the query returns every template that matches the <i>Identity</i> parameter.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument specified by the <i>SubFactor</i> parameter is not valid or a member of the structure specified by the <i>Identity</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_NO_RESULTS</b></b></dt>
</dl>
</td>
<td width="60%">
The query was successful, but no matching records could be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_LOCKED</b></b></dt>
</dl>
</td>
<td width="60%">
The database is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_READ_ERROR</b></b></dt>
</dl>
</td>
<td width="60%">
An unspecified problem occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b> or the <b>FileHandle</b> member is not valid.

</td>
</tr>
</table>
 




## -remarks



If this method returns successfully, the result set in the pipeline is replaced by the results of the query even if the query returns an empty set.

Callers of this function should be able to  retrieve all records by:

<ul>
<li>Passing a <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure in the <i>Identity</i> parameter with the  <b>Type</b> field set to  <b>WINBIO_IDENTITY_TYPE_WILDCARD</b>.</li>
<li>Passing <b>WINBIO_SUBTYPE_ANY</b> in the <i>SubFactor</i> parameter.</li>
</ul>
After a successful call to this function, the result set cursor should be  positioned on the first record in the set.

<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> parameter. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>

#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterQueryBySubject
//
// Purpose:
//      Locates templates that match a specified identity and sub-factor.
//
// Parameters:
//      Pipeline  -  Pointer to a WINBIO_PIPELINE structure associated with 
//                   the biometric unit performing the operation.
//      Identity  -  Pointer to a WINBIO_IDENTITY structure that contains the GUID 
//                   or SID to be located.
//      SubFactor -  A WINBIO_BIOMETRIC_SUBTYPE value that specifies the sub-factor 
//                   to be located.
//
static HRESULT
WINAPI
StorageAdapterQueryBySubject(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_IDENTITY Identity,
    __in WINBIO_BIOMETRIC_SUBTYPE SubFactor
    )
{
    HRESULT hr = S_OK;
    SIZE_T recordCount = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(Identity))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_STORAGE_CONTEXT storageContext = (PWINBIO_STORAGE_CONTEXT)Pipeline-&gt;StorageContext;

    // Verify the pipeline state.
    if (storageContext == NULL || storageContext-&gt;FileHandle == INVALID_HANDLE_VALUE)
    {
        hr =  WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Verify the Identity argument.
    if (Identity-&gt;Type != WINBIO_ID_TYPE_GUID &amp;&amp;
        Identity-&gt;Type != WINBIO_ID_TYPE_SID &amp;&amp;
        Identity-&gt;Type != WINBIO_ID_TYPE_WILDCARD)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    if (Identity-&gt;Type == WINBIO_ID_TYPE_WILDCARD &amp;&amp;
        Identity-&gt;Value.Wildcard != WINBIO_IDENTITY_WILDCARD)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // WINBIO_SUBTYPE_ANY is a valid sub-factor.
    // WINBIO_SUBTYPE_NO_INFORMATION is not a valid sub-factor.
    if (SubFactor == WINBIO_SUBTYPE_NO_INFORMATION)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Call a custom function (_FindAllMatchingRecords) that compares the 
    // identity and sub-factor values from the caller to the identity and
    // sub-factor values of every record in the database and adds the matching
    // database records to the result set in the pipeline.
    hr = _FindAllMatchingRecords( 
            Pipeline,
            Identity,
            SubFactor,
            &amp;recordCount
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }
    if (recordCount == 0)
    {
        hr = WINBIO_E_DATABASE_NO_RESULTS;
        goto cleanup;
    }

cleanup:

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/736688c3-2c2c-4244-9f49-98ad0fe2d141">StorageAdapterFirstRecord</a>



<a href="https://msdn.microsoft.com/a06550da-c6ea-44e5-b54f-8005bcbc0364">StorageAdapterGetCurrentRecord</a>



<a href="https://msdn.microsoft.com/dc7891c3-33f7-498c-acb1-4687909debb7">StorageAdapterGetRecordCount</a>



<a href="https://msdn.microsoft.com/e0025167-0778-474e-baca-ffc767822893">StorageAdapterNextRecord</a>



<a href="https://msdn.microsoft.com/773aacd1-a34a-4c5a-b615-2a5485f13ca1">StorageAdapterQueryByContent</a>
 

 

