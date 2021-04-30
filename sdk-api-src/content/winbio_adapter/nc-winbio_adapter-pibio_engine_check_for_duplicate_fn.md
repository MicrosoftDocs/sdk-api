---
UID: NC:winbio_adapter.PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN
title: PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN (winbio_adapter.h)
description: Determines whether a new template in the pipeline duplicates any template already saved in the database regardless of the identity associated with the templates.
helpviewer_keywords: ["EngineAdapterCheckForDuplicate","EngineAdapterCheckForDuplicate callback function [Windows Biometric Framework API]","PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN","PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN callback","secbiomet.engineadaptercheckforduplicate","winbio_adapter/EngineAdapterCheckForDuplicate"]
old-location: secbiomet\engineadaptercheckforduplicate.htm
tech.root: SecBioMet
ms.assetid: 0c73e8b3-2bec-419c-bcb0-3e35d1520f05
ms.date: 12/05/2018
ms.keywords: EngineAdapterCheckForDuplicate, EngineAdapterCheckForDuplicate callback function [Windows Biometric Framework API], PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN, PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN callback, secbiomet.engineadaptercheckforduplicate, winbio_adapter/EngineAdapterCheckForDuplicate
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN
 - winbio_adapter/PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterCheckForDuplicate
---

# PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN callback function


## -description

Called by the Windows Biometric Framework to determine whether a new template in the pipeline duplicates any template already saved in the database regardless of the identity associated with the templates.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Identity [out]

Pointer to a  <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that receives the GUID or SID of the duplicate template stored in the database.

### -param SubFactor [out]

Pointer to a  <b>WINBIO_BIOMETRIC_SUBTYPE</b> variable that receives the sub-factor associated with the duplicate template in the database.

### -param Duplicate [out]

A pointer to a Boolean value that specifies whether a matching template was found in the database.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
There is no enrollment template in the pipeline engine context.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function before committing a new enrollment template to the  database of a biometric unit. The purpose of this function is to prevent collisions in the engine adapter matching space. Collisions can result in false-positive matches.

This function should perform a content-based query by using the storage adapter to determine whether the template matches any template already in the database.


If this method finds a duplicate template in the database, it should return the <i>Identity</i> and <i>SubFactor</i> values for the matching template, set the <i>Duplicate</i> parameter to <b>TRUE</b>, and return an <b>HRESULT</b> value of S_OK.

If this method does not find a matching template in the database, it should set the  <i>Duplicate</i> parameter to <b>FALSE</b> but return an <b>HRESULT</b> value of S_OK.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterCheckForDuplicate
// 
// Purpose:
//      Determines whether a new template in the pipeline duplicates any 
//      template already saved in the database regardless of the identity 
//      associated with the templates.
//
// Parameters:
//      Pipeline    - Pointer to a WINBIO_PIPELINE structure associated 
//                    with the biometric unit performing the operation
//      Identity    - GUID or SID of the duplicate template stored in the 
//                    database
//      SubFactor   - sub-factor associated with the duplicate template in
//                    the database
//      Duplicate   - Boolean value that specifies whether a matching template 
//                    was found in the database
//
static HRESULT
WINAPI
EngineAdapterCheckForDuplicate(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_IDENTITY Identity,
    __out PWINBIO_BIOMETRIC_SUBTYPE SubFactor,
    __out PBOOLEAN Duplicate
    )
{
    HRESULT hr = S_OK;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    SIZE_T recordCount = 0;
    SIZE_T index = 0;
    WINBIO_STORAGE_RECORD thisRecord;
    BOOLEAN match = FALSE;
    DWORD indexVector[NUMBER_OF_TEMPLATE_BINS] = {0};

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline)  ||
        !ARGUMENT_PRESENT(Identity)  ||
        !ARGUMENT_PRESENT(SubFactor) ||
        !ARGUMENT_PRESENT(Duplicate))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // Return if an enrollment is not in progress. This example assumes that 
    // an enrollment object is part of your engine context structure.
    if (context->Enrollment.InProgress != TRUE)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Zero the memory pointed to by the Identity argument and set the
    // pointer to NULL.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Eliminate sub-factor information.
    *SubFactor  = WINBIO_SUBTYPE_NO_INFORMATION;

    // Initialize the Boolean Duplicate argument to FALSE.
    *Duplicate  = FALSE;

    // If your adapter supports index vectors to place templates into buckets,
    // call a custom function (_AdapterCreateIndexVector) to create an index 
    // vector from the template data in the feature set. In this example, the
    // engine adapter context attached to the pipeline contains an Enrollment
    // member that references the current template. Your implementation may
    // differ.
    hr = _AdapterCreateIndexVector(
                context, 
                context->Enrollment.Template, 
                context->Enrollment.TemplateSize,
                indexVector, 
                NUMBER_OF_TEMPLATE_BINS, 
                &rejectDetail
                );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Retrieve the records in the index vector. If your adapter does not support 
    // index vectors (the vector length is zero), calling the WbioStorageQueryByContent 
    // function will retrieve all records.
    // WbioStorageQueryByContent is a wrapper function in the Winbio_adapter.h 
    // header file.
    hr = WbioStorageQueryByContent(
            Pipeline,
            WINBIO_SUBTYPE_ANY,
            indexVector,
            NUMBER_OF_TEMPLATE_BINS
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Determine the size of the result set. WbioStorageGetRecordCount is a wrapper
    // function in the Winbio_adapter.h header file.
    hr = WbioStorageGetRecordCount( Pipeline, &recordCount);
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Point the result set cursor at the first record. WbioStorageFirstRecord
    // is a wrapper function in the Winbio_adapter.h header file.
    hr = WbioStorageFirstRecord( Pipeline );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Iterate through all records in the result set and determine which record
    // matches the current feature set. WbioStorageGetCurrentRecord is a wrapper
    // function in the Winbio_adapter.h header file. 
    for (index = 0; index < recordCount; ++index)
    {
        hr = WbioStorageGetCurrentRecord( Pipeline, &thisRecord );
        if (FAILED(hr))
        {
            goto cleanup;
        }

        // Call a custom function (_AdapterCompareTemplateToCurrentFeatureSet) to
        // compare the feature set attached to the pipeline with the template
        // retrieved from storage.
        // If the template and feature set match, return S_OK and set the match
        // argument to TRUE. If the template and feature set do not match, return
        // S_OK and set the match argument to FALSE. If the function fails for some
        // other reason, return a failure HRESULT.
        hr = _AdapterCompareTemplateToEnrollmentTemplate( 
                    context, 
                    context->Enrollment.Template, 
                    context->Enrollment.TemplateSize,
                    thisRecord.TemplateBlob, 
                    thisRecord.TemplateBlobSize,
                    &match
                    );
        if (FAILED(hr))
        {
            goto cleanup;
        }
        if (match)
        {
            break;
        }

        // Retrieve the next record.
        hr = WbioStorageNextRecord( Pipeline );
        if (FAILED(hr))
        {
            if (hr == WINBIO_E_DATABASE_NO_MORE_RECORDS)
            {
                hr = S_OK;
                break;
            }
            else
            {
                goto cleanup;
            }
        }
    }

    // If there is a duplicate template in the database, return information about
    // it to the caller.
    if (match)
    {
        CopyMemory( Identity, thisRecord.Identity, sizeof(WINBIO_IDENTITY));
        *SubFactor = thisRecord.SubFactor;
        *Duplicate = TRUE;
        hr = S_OK;
    }

cleanup:

    // There are no duplicates. This is an acceptable result.
    if (hr == WINBIO_E_DATABASE_NO_RESULTS)
    {
        hr = S_OK;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>