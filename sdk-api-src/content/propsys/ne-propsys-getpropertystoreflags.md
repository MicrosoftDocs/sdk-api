---
UID: NE:propsys.GETPROPERTYSTOREFLAGS
title: GETPROPERTYSTOREFLAGS (propsys.h)
description: Indicates flags that modify the property store object retrieved by methods that create a property store, such as IShellItem2::GetPropertyStore or IPropertyStoreFactory::GetPropertyStore.
helpviewer_keywords: ["GETPROPERTYSTOREFLAGS","GETPROPERTYSTOREFLAGS enumeration [Windows Properties]","GPS_BESTEFFORT","GPS_DEFAULT","GPS_DELAYCREATION","GPS_EXTRINSICPROPERTIES","GPS_EXTRINSICPROPERTIESONLY","GPS_FASTPROPERTIESONLY","GPS_HANDLERPROPERTIESONLY","GPS_MASK_VALID","GPS_NO_OPLOCK","GPS_OPENSLOWITEM","GPS_PREFERQUERYPROPERTIES","GPS_READWRITE","GPS_TEMPORARY","_shell_GETPROPERTYSTOREFLAGS","properties.GETPROPERTYSTOREFLAGS","propsys/GETPROPERTYSTOREFLAGS","propsys/GPS_BESTEFFORT","propsys/GPS_DEFAULT","propsys/GPS_DELAYCREATION","propsys/GPS_EXTRINSICPROPERTIES","propsys/GPS_EXTRINSICPROPERTIESONLY","propsys/GPS_FASTPROPERTIESONLY","propsys/GPS_HANDLERPROPERTIESONLY","propsys/GPS_MASK_VALID","propsys/GPS_NO_OPLOCK","propsys/GPS_OPENSLOWITEM","propsys/GPS_PREFERQUERYPROPERTIES","propsys/GPS_READWRITE","propsys/GPS_TEMPORARY","shell.GETPROPERTYSTOREFLAGS"]
old-location: properties\GETPROPERTYSTOREFLAGS.htm
tech.root: properties
ms.assetid: d3fde1b9-b19f-431d-9cea-bffc289ee683
ms.date: 12/05/2018
ms.keywords: GETPROPERTYSTOREFLAGS, GETPROPERTYSTOREFLAGS enumeration [Windows Properties], GPS_BESTEFFORT, GPS_DEFAULT, GPS_DELAYCREATION, GPS_EXTRINSICPROPERTIES, GPS_EXTRINSICPROPERTIESONLY, GPS_FASTPROPERTIESONLY, GPS_HANDLERPROPERTIESONLY, GPS_MASK_VALID, GPS_NO_OPLOCK, GPS_OPENSLOWITEM, GPS_PREFERQUERYPROPERTIES, GPS_READWRITE, GPS_TEMPORARY, _shell_GETPROPERTYSTOREFLAGS, properties.GETPROPERTYSTOREFLAGS, propsys/GETPROPERTYSTOREFLAGS, propsys/GPS_BESTEFFORT, propsys/GPS_DEFAULT, propsys/GPS_DELAYCREATION, propsys/GPS_EXTRINSICPROPERTIES, propsys/GPS_EXTRINSICPROPERTIESONLY, propsys/GPS_FASTPROPERTIESONLY, propsys/GPS_HANDLERPROPERTIESONLY, propsys/GPS_MASK_VALID, propsys/GPS_NO_OPLOCK, propsys/GPS_OPENSLOWITEM, propsys/GPS_PREFERQUERYPROPERTIES, propsys/GPS_READWRITE, propsys/GPS_TEMPORARY, shell.GETPROPERTYSTOREFLAGS
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GETPROPERTYSTOREFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GETPROPERTYSTOREFLAGS
 - propsys/GETPROPERTYSTOREFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - GETPROPERTYSTOREFLAGS
---

# GETPROPERTYSTOREFLAGS enumeration


## -description

Indicates flags that modify the property store object retrieved by methods that create a property store, such as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a> or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore">IPropertyStoreFactory::GetPropertyStore</a>.

## -enum-fields

### -field GPS_DEFAULT:0

Meaning to a calling process: Return a read-only property store that contains all properties. Slow items (offline files) are not opened. 
			    
                

Combination with other flags: Can be overridden by other flags.

### -field GPS_HANDLERPROPERTIESONLY:0x1

Meaning to a calling process: Include only properties directly from the property handler, which opens the file on the disk, network, or device. 

			    

Meaning to a file folder: Only include properties directly from the handler.

Meaning to other folders: When delegating to a file folder, pass this flag on to the file folder; do not do any multiplexing (MUX). When not delegating to a file folder, ignore this flag instead of returning a failure code.

Combination with other flags: Cannot be combined with GPS_TEMPORARY, GPS_FASTPROPERTIESONLY, or GPS_BESTEFFORT.

### -field GPS_READWRITE:0x2

Meaning to a calling process: Can write properties to the item. Note: The store may contain fewer properties than a read-only store.
			
                

Meaning to a file folder: ReadWrite.

Meaning to other folders: ReadWrite. Note: When using default MUX, return a single unmultiplexed store because the default MUX does not support ReadWrite.

Combination with other flags: Cannot be combined with GPS_TEMPORARY, GPS_FASTPROPERTIESONLY, GPS_BESTEFFORT, or GPS_DELAYCREATION. Implies GPS_HANDLERPROPERTIESONLY.

### -field GPS_TEMPORARY:0x4

Meaning to a calling process: Provides a writable store, with no initial properties, that exists for the lifetime of the Shell item instance; basically, a property bag attached to the item instance.
			
                

Meaning to a file folder: Not applicable. Handled by the Shell item.

Meaning to other folders: Not applicable. Handled by the Shell item.

Combination with other flags: Cannot be combined with any other flag. Implies GPS_READWRITE.

### -field GPS_FASTPROPERTIESONLY:0x8

Meaning to a calling process: Provides a store that does not involve reading from the disk or network. Note: Some values may be different, or missing, compared to a store without this flag.
			
                

Meaning to a file folder: Include the "innate" and "fallback" stores only. Do not load the handler.

Meaning to other folders: Include only properties that are available in memory or can be computed very quickly (no properties from disk, network, or peripheral IO devices). This is normally only data sources from the IDLIST. When delegating to other folders, pass this flag on to them.

Combination with other flags: Cannot be combined with GPS_TEMPORARY, GPS_READWRITE, GPS_HANDLERPROPERTIESONLY, or GPS_DELAYCREATION.

### -field GPS_OPENSLOWITEM:0x10

Meaning to a calling process: Open a slow item (offline file) if necessary.
			    
                

Meaning to a file folder: Retrieve a file from offline storage, if necessary. Note: Without this flag, the handler is not created for offline files.

Meaning to other folders: Do not return any properties that are very slow.

Combination with other flags: Cannot be combined with GPS_TEMPORARY or GPS_FASTPROPERTIESONLY.

### -field GPS_DELAYCREATION:0x20

Meaning to a calling process: Delay memory-intensive operations, such as file access, until a property is requested that requires such access.
			    
                

Meaning to a file folder: Do not create the handler until needed; for example, either <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GetCount</a>/<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresourcecollection-getat">GetAt</a> or <a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">GetValue</a>, where the innate store does not satisfy the request. Note: <b>GetValue</b> might fail due to file access problems.

Meaning to other folders: If the folder has memory-intensive properties, such as delegating to a file folder or network access, it can optimize performance by supporting <a href="/windows/desktop/api/propsys/nn-propsys-idelayedpropertystorefactory">IDelayedPropertyStoreFactory</a> and splitting up its properties into a fast and a slow store. It can then use delayed MUX to recombine them.

Combination with other flags: Cannot be combined with GPS_TEMPORARY or GPS_READWRITE.

### -field GPS_BESTEFFORT:0x40

Meaning to a calling process: Succeed at getting the store, even if some properties are not returned. Note: Some values may be different, or missing, compared to a store without this flag.
			    
                

Meaning to a file folder: Succeed and return a store, even if the handler or innate store has an error during creation. Only fail if substores fail.

Meaning to other folders: Succeed on getting the store, even if some properties are not returned.

Combination with other flags: Cannot be combined with GPS_TEMPORARY, GPS_READWRITE, or GPS_HANDLERPROPERTIESONLY.

### -field GPS_NO_OPLOCK:0x80

<b>Windows 7 and later</b>. Callers should use this flag only if they are already holding an opportunistic lock (oplock) on the file because without an oplock, the bind operation cannot continue. By default, the Shell requests an oplock on a file before binding to the property handler. This flag disables the default behavior. 

<b>Windows Server 2008 and Windows Vista:  </b>This flag is not available.

### -field GPS_PREFERQUERYPROPERTIES:0x100

<b>Windows 8 and later</b>. Use this flag to retrieve only properties from the indexer for WDS results.

### -field GPS_EXTRINSICPROPERTIES:0x200

Include properties from the file's secondary stream.

### -field GPS_EXTRINSICPROPERTIESONLY:0x400

Include only properties from the file's secondary stream.

### -field GPS_VOLATILEPROPERTIES:0x800

### -field GPS_VOLATILEPROPERTIESONLY:0x1000

### -field GPS_MASK_VALID:0x1fff

Mask for valid <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> values.

## -remarks

If the Shell item is a file, the property store contains the following items. 
                
                

<ul>
<li>Properties from the file system that concern the file.</li>
<li>Properties from the file itself that are provided by the file's property handler, unless the file is offline (see GPS_OPENSLOWITEM).</li>
</ul>
Non-file Shell items return a similar read-only store.

<div class="alert"><b>Note</b>  GPS_INCLUDEOFFLINEPROPERTIES has been superseded by GPS_OPENSLOWITEM.</div>
<div> </div>
