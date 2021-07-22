---
UID: NF:rometadataapi.IMetaDataDispenserEx.SetOption
title: IMetaDataDispenserEx::SetOption (rometadataapi.h)
description: Sets the specified option to a given value for the current metadata scope. The option controls how calls to the current metadata scope are handled.
helpviewer_keywords: ["IMetaDataDispenserEx interface [Windows Runtime]","SetOption method","IMetaDataDispenserEx.SetOption","IMetaDataDispenserEx::SetOption","SetOption","SetOption method [Windows Runtime]","SetOption method [Windows Runtime]","IMetaDataDispenserEx interface","rometadataapi/IMetaDataDispenserEx::SetOption","winrt.imetadatadispenserex_setoption"]
old-location: winrt\imetadatadispenserex_setoption.htm
tech.root: WinRT
ms.assetid: bb84abf1-0bba-4f9d-98fb-3ed67819a9dc
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenserEx interface [Windows Runtime],SetOption method, IMetaDataDispenserEx.SetOption, IMetaDataDispenserEx::SetOption, SetOption, SetOption method [Windows Runtime], SetOption method [Windows Runtime],IMetaDataDispenserEx interface, rometadataapi/IMetaDataDispenserEx::SetOption, winrt.imetadatadispenserex_setoption
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataDispenserEx::SetOption
 - rometadataapi/IMetaDataDispenserEx::SetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx.SetOption
---

# IMetaDataDispenserEx::SetOption


## -description

Sets the specified option to a given value for the current metadata scope. The option controls how calls to the current metadata scope are handled.

## -parameters

### -param optionId [in]

 A pointer to a GUID that specifies the option to be set.

### -param pValue [in]

The value to use to set the option. The type of this value must be a variant of the specified option's type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following table lists the available GUIDs that the <i>optionId</i> parameter can point to and the corresponding valid values for the <i>pValue</i> parameter.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
<th><i>pValue</i> Parameter</th>
</tr>
<tr>
<td>MetaDataCheckDuplicatesFor</td>
<td>Controls which items are checked for duplicates.</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/corcheckduplicatesfor-enumeration">CorCheckDuplicatesFor</a> enumeration.</td>
</tr>
<tr>
<td>MetaDataRefToDefCheck
</td>
<td>Controls which referenced items are converted to definitions. By default, the metadata engine will optimize the code by converting a referenced item to its definition if the referenced item is actually defined in the current scope.
</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/correftodefcheck-enumeration">CorRefToDefCheck</a> enumeration.
</td>
</tr>
<tr>
<td>MetaDataNotificationForTokenMovement
</td>
<td>Controls which token remaps occurring during a metadata merge generate callbacks. </td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/cornotificationfortokenmovement-enumeration">CorNotificationForTokenMovement</a> enumeration.
</td>
</tr>
<tr>
<td>MetaDataSetENC
</td>
<td>Controls the behavior of edit-and-continue (ENC). Only one mode of behavior can be set at a time.
</td>
<td>Must be a variant of type UI4, and must contain a value of the <a href="/dotnet/framework/unmanaged-api/metadata/corsetenc-enumeration">CorSetENC</a> enumeration. The value is not a bitmask.
</td>
</tr>
<tr>
<td>MetaDataErrorIfEmitOutOfOrder
</td>
<td>Controls which emitted-out-of-order errors generate callbacks. Emitting metadata out of order is not fatal; however, if you emit metadata in an order that is favored by the metadata engine, the metadata is more compact and therefore can be more efficiently searched.</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/corerrorifemitoutoforder-enumeration">CorErrorIfEmitOutOfOrder</a> enumeration.
</td>
</tr>
<tr>
<td>MetaDataImportOption
</td>
<td>Controls which kinds of items that were deleted during an ENC are retrieved by an enumerator.
</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/corimportoptions-enumeration">CorImportOptions</a> enumeration.
</td>
</tr>
<tr>
<td>MetaDataThreadSafetyOptions
</td>
<td>Controls whether the metadata engine obtains reader/writer locks, thereby ensuring thread safety. By default, the engine assumes that access is single-threaded by the caller, so no locks are obtained. Clients are responsible for maintaining proper thread synchronization when using the metadata API.
</td>
<td>Must be a variant of type UI4, and must contain a value of the <a href="/dotnet/framework/unmanaged-api/metadata/corthreadsafetyoptions-enumeration">CorThreadSafetyOptions</a> enumeration. The value is not a bitmask.
</td>
</tr>
<tr>
<td>MetaDataGenerateTCEAdapters
</td>
<td>Controls whether the type library importer should generate the tightly coupled event (TCE) adapters for COM connection point containers.
</td>
<td>Must be a variant of type BOOL. If <i>pValue</i> is set to <b>true</b>, the type library importer generates the TCE adapters.
</td>
</tr>
<tr>
<td>MetaDataTypeLibImportNamespace
</td>
<td>Specifies a non-default namespace for the type library that is being imported.
</td>
<td>Must be either a null value or a variant of type BSTR. If <i>pValue</i> is a null value, the current namespace is set to null; otherwise, the current namespace is set to the string that is held in the variant's BSTR type.
</td>
</tr>
<tr>
<td>MetaDataLinkerOptions
</td>
<td>Controls whether the linker should generate an assembly or a .NET Framework module file.
</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the <a href="/dotnet/framework/unmanaged-api/metadata/corlinkeroptions-enumeration">CorLinkerOptions</a> enumeration.
</td>
</tr>
<tr>
<td>MetaDataRuntimeVersion
</td>
<td>Specifies the version of the common language runtime against which this image was built. The version is stored as a string, such as "v1.0.3705".
</td>
<td>Must be a null value, a VT_EMPTY value, or a variant of type BSTR. If <i>pValue</i> is null, the runtime version is set to null. If <i>pValue</i> is VT_EMPTY, the version is set to a default value, which is drawn from the version of Mscorwks.dll within which the metadata code is running. Otherwise, the runtime version is set to the string that is held in the variant's BSTR type.
</td>
</tr>
<tr>
<td>MetaDataMergerOptions
</td>
<td>Specifies options for merging metadata.
</td>
<td>Must be a variant of type UI4, and must contain a combination of the values of the MergeFlags enumeration, which is described in the CorHdr.h file.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>