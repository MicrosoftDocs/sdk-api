---
UID: TP:shell
ms.assetid: 2827809d-7ca5-313d-944e-507165c995d8
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# The Windows Shell



Overview of the The Windows Shell technology.

To develop The Windows Shell, you need these headers:

 * [appmgmt.h](..\appmgmt\index.md)
 * [appnotify.h](..\appnotify\index.md)
 * [cpl.h](..\cpl\index.md)
 * [credentialprovider.h](..\credentialprovider\index.md)
 * [dimm.h](..\dimm\index.md)
 * [imagetranscode.h](..\imagetranscode\index.md)
 * [inputpanelconfiguration.h](..\inputpanelconfiguration\index.md)
 * [intsafe.h](..\intsafe\index.md)
 * [intshcut.h](..\intshcut\index.md)
 * [mobsync.h](..\mobsync\index.md)
 * [objectarray.h](..\objectarray\index.md)
 * [pathcch.h](..\pathcch\index.md)
 * [profinfo.h](..\profinfo\index.md)
 * [propkeydef.h](..\propkeydef\index.md)
 * [scrnsave.h](..\scrnsave\index.md)
 * [shappmgr.h](..\shappmgr\index.md)
 * [shdeprecated.h](..\shdeprecated\index.md)
 * [shidfact.h](..\shidfact\index.md)
 * [shimgdata.h](..\shimgdata\index.md)
 * [shlobj_core.h](..\shlobj_core\index.md)
 * [shlwapi.h](..\shlwapi\index.md)
 * [shtypes.h](..\shtypes\index.md)
 * [storageprovider.h](..\storageprovider\index.md)
 * [syncmgr.h](..\syncmgr\index.md)
 * [thumbcache.h](..\thumbcache\index.md)
 * [thumbnailstreamcache.h](..\thumbnailstreamcache\index.md)
 * [tlogstg.h](..\tlogstg\index.md)
 * [userenv.h](..\userenv\index.md)

For the programming guide, see [The Windows Shell](https://review.docs.microsoft.com/en-us/win32-test/shell).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AssocCreate function](..\shlwapi\nf-shlwapi-assoccreate.md) | Returns a pointer to an IQueryAssociations object. |
| [AssocGetDetailsOfPropKey function](..\shlobj_core\nf-shlobj_core-assocgetdetailsofpropkey.md) | Retrieves the value for a given property key using the file association information provided by the Namespace Extensions. |
| [AssocGetPerceivedType function](..\shlwapi\nf-shlwapi-assocgetperceivedtype.md) | Retrieves a file's perceived type based on its extension. |
| [AssocIsDangerous function](..\shlwapi\nf-shlwapi-associsdangerous.md) | Determines whether a file type is considered a potential security risk. |
| [AssocQueryKeyA function](..\shlwapi\nf-shlwapi-assocquerykeya.md) | Searches for and retrieves a key related to a file or protocol association from the registry. |
| [AssocQueryKeyW function](..\shlwapi\nf-shlwapi-assocquerykeyw.md) | Searches for and retrieves a key related to a file or protocol association from the registry. |
| [AssocQueryStringA function](..\shlwapi\nf-shlwapi-assocquerystringa.md) | Searches for and retrieves a file or protocol association-related string from the registry. |
| [AssocQueryStringByKeyA function](..\shlwapi\nf-shlwapi-assocquerystringbykeya.md) | Searches for and retrieves a file association-related string from the registry starting from a specified key. |
| [AssocQueryStringByKeyW function](..\shlwapi\nf-shlwapi-assocquerystringbykeyw.md) | Searches for and retrieves a file association-related string from the registry starting from a specified key. |
| [AssocQueryStringW function](..\shlwapi\nf-shlwapi-assocquerystringw.md) | Searches for and retrieves a file or protocol association-related string from the registry. |
| [ByteToChar function](..\intsafe\nf-intsafe-bytetochar.md) | Converts a value of type BYTE to a value of type CHAR. |
| [ByteToInt8 function](..\intsafe\nf-intsafe-bytetoint8.md) | Converts a value of type BYTE to a value of type INT8. |
| [CDefFolderMenu_Create2 function](..\shlobj_core\nf-shlobj_core-cdeffoldermenu_create2.md) | Creates a context menu for a selected group of file folder objects. |
| [CIDLData_CreateFromIDArray function](..\shlobj_core\nf-shlobj_core-cidldata_createfromidarray.md) | CIDLData_CreateFromIDArray may be altered or unavailable. |
| [ChrCmpIA function](..\shlwapi\nf-shlwapi-chrcmpia.md) | Performs a comparison between two characters. The comparison is not case-sensitive. |
| [ChrCmpIW function](..\shlwapi\nf-shlwapi-chrcmpiw.md) | Performs a comparison between two characters. The comparison is not case-sensitive. |
| [ColorAdjustLuma function](..\shlwapi\nf-shlwapi-coloradjustluma.md) | Changes the luminance of a RGB value. Hue and saturation are not affected. |
| [ColorHLSToRGB function](..\shlwapi\nf-shlwapi-colorhlstorgb.md) | Converts colors from hue-luminance-saturation (HLS) to RGB format. |
| [ColorRGBToHLS function](..\shlwapi\nf-shlwapi-colorrgbtohls.md) | Converts colors from RGB to hue-luminance-saturation (HLS) format. |
| [ConnectToConnectionPoint function](..\shlwapi\nf-shlwapi-connecttoconnectionpoint.md) | Establishes or terminates a connection between a client's sink and a connection point container. |
| [CreateAppContainerProfile function](..\userenv\nf-userenv-createappcontainerprofile.md) | Creates a per-user, per-app profile for Windows Store apps. |
| [CreateEnvironmentBlock function](..\userenv\nf-userenv-createenvironmentblock.md) | Retrieves the environment variables for the specified user. This block can then be passed to the CreateProcessAsUser function. |
| [CreateProfile function](..\userenv\nf-userenv-createprofile.md) | Creates a new user profile. |
| [DAD_AutoScroll function](..\shlobj_core\nf-shlobj_core-dad_autoscroll.md) | Scrolls the window while an image is being dragged. |
| [DAD_DragEnterEx function](..\shlobj_core\nf-shlobj_core-dad_dragenterex.md) | Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. |
| [DAD_DragEnterEx2 function](..\shlobj_core\nf-shlobj_core-dad_dragenterex2.md) | Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window. |
| [DAD_DragLeave function](..\shlobj_core\nf-shlobj_core-dad_dragleave.md) | Unlocks the window locked by the DAD_DragEnterEx function. |
| [DAD_DragMove function](..\shlobj_core\nf-shlobj_core-dad_dragmove.md) | Moves the image that is being dragged during a drag-and-drop operation. |
| [DAD_SetDragImage function](..\shlobj_core\nf-shlobj_core-dad_setdragimage.md) | Sets the drag image. |
| [DAD_ShowDragImage function](..\shlobj_core\nf-shlobj_core-dad_showdragimage.md) | Shows or hides the image being dragged. |
| [DWordPtrAdd function](..\intsafe\nf-intsafe-dwordptradd.md) | Adds two values of type DWORD_PTR. |
| [DWordPtrMult function](..\intsafe\nf-intsafe-dwordptrmult.md) | Multiplies one value of type DWORD_PTR by another. |
| [DWordPtrSub function](..\intsafe\nf-intsafe-dwordptrsub.md) | Subtracts one value of type DWORD_PTR from another. |
| [DefScreenSaverProc function](..\scrnsave\nf-scrnsave-defscreensaverproc.md) | Provides default processing for any messages that a screen saver application does not process. |
| [DeleteAppContainerProfile function](..\userenv\nf-userenv-deleteappcontainerprofile.md) | Deletes the specified per-user, per-app profile. |
| [DeleteProfileA function](..\userenv\nf-userenv-deleteprofilea.md) | Deletes the user profile and all user-related settings from the specified computer. The caller must have administrative privileges to delete a user's profile. |
| [DeleteProfileW function](..\userenv\nf-userenv-deleteprofilew.md) | Deletes the user profile and all user-related settings from the specified computer. The caller must have administrative privileges to delete a user's profile. |
| [DeriveAppContainerSidFromAppContainerName function](..\userenv\nf-userenv-deriveappcontainersidfromappcontainername.md) | Gets the SID of the specified profile. |
| [DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName function](..\userenv\nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname.md) | DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName is reserved for future use. |
| [DestroyEnvironmentBlock function](..\userenv\nf-userenv-destroyenvironmentblock.md) | Frees environment variables created by the CreateEnvironmentBlock function. |
| [DllInstall function](..\shlwapi\nf-shlwapi-dllinstall.md) | Handles installation and setup for a DLL. |
| [DriveType function](..\shlobj_core\nf-shlobj_core-drivetype.md) | DriveType may be altered or unavailable. |
| [ExpandEnvironmentStringsForUserA function](..\userenv\nf-userenv-expandenvironmentstringsforusera.md) | Expands the source string by using the environment block established for the specified user. |
| [ExpandEnvironmentStringsForUserW function](..\userenv\nf-userenv-expandenvironmentstringsforuserw.md) | Expands the source string by using the environment block established for the specified user. |
| [FreeConfirmConflictItem function](..\syncmgr\nf-syncmgr-freeconfirmconflictitem.md) | Frees the resources that have been allocated for a CONFIRM_CONFLICT_ITEM structure. |
| [GetAcceptLanguagesA function](..\shlwapi\nf-shlwapi-getacceptlanguagesa.md) | Retrieves a string used with websites when specifying language preferences. |
| [GetAcceptLanguagesW function](..\shlwapi\nf-shlwapi-getacceptlanguagesw.md) | Retrieves a string used with websites when specifying language preferences. |
| [GetAllUsersProfileDirectoryA function](..\userenv\nf-userenv-getallusersprofiledirectorya.md) | Retrieves the path to the root of the directory that contains program data shared by all users. |
| [GetAllUsersProfileDirectoryW function](..\userenv\nf-userenv-getallusersprofiledirectoryw.md) | Retrieves the path to the root of the directory that contains program data shared by all users. |
| [GetAppContainerFolderPath function](..\userenv\nf-userenv-getappcontainerfolderpath.md) | Gets the path of the local app data folder for the specified app container. |
| [GetAppContainerRegistryLocation function](..\userenv\nf-userenv-getappcontainerregistrylocation.md) | Gets the location of the registry storage associated with an app container. |
| [GetDefaultUserProfileDirectoryA function](..\userenv\nf-userenv-getdefaultuserprofiledirectorya.md) | Retrieves the path to the root of the default user's profile. |
| [GetDefaultUserProfileDirectoryW function](..\userenv\nf-userenv-getdefaultuserprofiledirectoryw.md) | Retrieves the path to the root of the default user's profile. |
| [GetDetailsOf function](..\shlobj_core\nf-shlobj_core-getdetailsof.md) | Retrieves details about an item in a folder. For example, its size, type, or the time of its last modification. |
| [GetFileNameFromBrowse function](..\shlobj_core\nf-shlobj_core-getfilenamefrombrowse.md) | Creates an Open dialog box so that the user can specify the drive, directory, and name of a file to open. |
| [GetIconLocation function](..\shlobj_core\nf-shlobj_core-geticonlocation.md) | Gets the location of the icon assigned to the link. |
| [GetMenuPosFromID function](..\shlwapi\nf-shlwapi-getmenuposfromid.md) | GetMenuPosFromID may be altered or unavailable. |
| [GetProcessReference function](..\shlwapi\nf-shlwapi-getprocessreference.md) | Retrieves the process-specific object supplied by SetProcessReference, incrementing the reference count to keep the process alive. |
| [GetProfileType function](..\userenv\nf-userenv-getprofiletype.md) | Retrieves the type of profile loaded for the current user. |
| [GetProfilesDirectoryA function](..\userenv\nf-userenv-getprofilesdirectorya.md) | Retrieves the path to the root directory where user profiles are stored. |
| [GetProfilesDirectoryW function](..\userenv\nf-userenv-getprofilesdirectoryw.md) | Retrieves the path to the root directory where user profiles are stored. |
| [GetUserProfileDirectoryA function](..\userenv\nf-userenv-getuserprofiledirectorya.md) | Retrieves the path to the root directory of the specified user's profile. |
| [GetUserProfileDirectoryW function](..\userenv\nf-userenv-getuserprofiledirectoryw.md) | Retrieves the path to the root directory of the specified user's profile. |
| [HashData function](..\shlwapi\nf-shlwapi-hashdata.md) | Hashes an array of data. |
| [IDListContainerIsConsistent function](..\shlobj_core\nf-shlobj_core-idlistcontainerisconsistent.md) | Verifies that the container structure of an IDList is valid. |
| [ILAppendID function](..\shlobj_core\nf-shlobj_core-ilappendid.md) | Appends or prepends an SHITEMID structure to an ITEMIDLIST structure. |
| [ILClone function](..\shlobj_core\nf-shlobj_core-ilclone.md) | Clones an ITEMIDLIST structure. |
| [ILCloneChild function](..\shlobj_core\nf-shlobj_core-ilclonechild.md) | Clones a child ITEMIDLIST structure. |
| [ILCloneFirst function](..\shlobj_core\nf-shlobj_core-ilclonefirst.md) | Clones the first SHITEMID structure in an ITEMIDLIST structure. |
| [ILCloneFull function](..\shlobj_core\nf-shlobj_core-ilclonefull.md) | Clones a full, or absolute, ITEMIDLIST structure. |
| [ILCombine function](..\shlobj_core\nf-shlobj_core-ilcombine.md) | Combines two ITEMIDLIST structures. |
| [ILCreateFromPath function](..\shlobj_core\nf-shlobj_core-ilcreatefrompath.md) | Returns the ITEMIDLIST structure associated with a specified file path. |
| [ILCreateFromPathA function](..\shlobj_core\nf-shlobj_core-ilcreatefrompatha.md) | Returns the ITEMIDLIST structure associated with a specified file path. |
| [ILCreateFromPathW function](..\shlobj_core\nf-shlobj_core-ilcreatefrompathw.md) | Returns the ITEMIDLIST structure associated with a specified file path. |
| [ILFindChild function](..\shlobj_core\nf-shlobj_core-ilfindchild.md) | Determines whether a specified ITEMIDLIST structure is the child of another ITEMIDLIST structure. |
| [ILFindLastID function](..\shlobj_core\nf-shlobj_core-ilfindlastid.md) | Returns a pointer to the last SHITEMID structure in an ITEMIDLIST structure. |
| [ILFree function](..\shlobj_core\nf-shlobj_core-ilfree.md) | Frees an ITEMIDLIST structure allocated by the Shell. |
| [ILGetNext function](..\shlobj_core\nf-shlobj_core-ilgetnext.md) | Retrieves the next SHITEMID structure in an ITEMIDLIST structure. |
| [ILGetSize function](..\shlobj_core\nf-shlobj_core-ilgetsize.md) | Returns the size, in bytes, of an ITEMIDLIST structure. |
| [ILIsAligned function](..\shlobj_core\nf-shlobj_core-ilisaligned.md) | Verifies whether a constant ITEMIDLIST is aligned on a pointer boundary, which is a DWORD on 32-bit architectures and a QWORD on 64-bit architectures. |
| [ILIsChild function](..\shlobj_core\nf-shlobj_core-ilischild.md) | Verifies whether a pointer to an item identifier list (PIDL) is a child PIDL, which is a PIDL with exactly one SHITEMID. |
| [ILIsEmpty function](..\shlobj_core\nf-shlobj_core-ilisempty.md) | Verifies whether an ITEMIDLIST structure is empty. |
| [ILIsEqual function](..\shlobj_core\nf-shlobj_core-ilisequal.md) | Tests whether two ITEMIDLIST structures are equal in a binary comparison. |
| [ILIsParent function](..\shlobj_core\nf-shlobj_core-ilisparent.md) | Tests whether an ITEMIDLIST structure is the parent of another ITEMIDLIST structure. |
| [ILLoadFromStream function](..\shlobj_core\nf-shlobj_core-illoadfromstream.md) | Deprecated. Loads an ITEMIDLIST structure from a stream. |
| [ILLoadFromStreamEx function](..\shlobj_core\nf-shlobj_core-illoadfromstreamex.md) | This function may be altered or unavailable. |
| [ILNext function](..\shlobj_core\nf-shlobj_core-ilnext.md) | Retrieves the next SHITEMID structure in an ITEMIDLIST structure. |
| [ILRemoveLastID function](..\shlobj_core\nf-shlobj_core-ilremovelastid.md) | Removes the last SHITEMID structure from an ITEMIDLIST structure. |
| [ILSaveToStream function](..\shlobj_core\nf-shlobj_core-ilsavetostream.md) | Saves an ITEMIDLIST structure to a stream. |
| [ILSkip function](..\shlobj_core\nf-shlobj_core-ilskip.md) | Skips a given number of bytes in a constant, unaligned, relative ITEMIDLIST structure. |
| [IStream_Copy function](..\shlwapi\nf-shlwapi-istream_copy.md) | Copies a stream to another stream. |
| [IStream_Read function](..\shlwapi\nf-shlwapi-istream_read.md) | Reads bytes from a specified stream and returns a value that indicates whether all bytes were successfully read. |
| [IStream_ReadPidl function](..\shlwapi\nf-shlwapi-istream_readpidl.md) | Reads a pointer to an item identifier list (PIDL) from an IStream object into a PIDLIST_RELATIVE object. |
| [IStream_ReadStr function](..\shlwapi\nf-shlwapi-istream_readstr.md) | Reads from a stream and writes into a string. |
| [IStream_Reset function](..\shlwapi\nf-shlwapi-istream_reset.md) | Moves the seek position in a specified stream to the beginning of the stream. |
| [IStream_Size function](..\shlwapi\nf-shlwapi-istream_size.md) | Retrieves the size, in bytes, of a specified stream. |
| [IStream_Write function](..\shlwapi\nf-shlwapi-istream_write.md) | Writes data of unknown format from a buffer to a specified stream. |
| [IStream_WritePidl function](..\shlwapi\nf-shlwapi-istream_writepidl.md) | Writes a pointer to an item identifier list (PIDL) from a PCUIDLIST_RELATIVE object into an IStream object. |
| [IStream_WriteStr function](..\shlwapi\nf-shlwapi-istream_writestr.md) | Reads from a string and writes into a stream. |
| [IUnknown_AtomicRelease function](..\shlwapi\nf-shlwapi-iunknown_atomicrelease.md) | Releases a Component Object Model (COM) pointer and sets it to NULL. |
| [IUnknown_GetSite function](..\shlwapi\nf-shlwapi-iunknown_getsite.md) | Calls the specified object's IObjectWithSite |
| [IUnknown_GetWindow function](..\shlwapi\nf-shlwapi-iunknown_getwindow.md) | Attempts to retrieve a window handle from a Component Object Model (COM) object by querying for various interfaces that have a GetWindow method. |
| [IUnknown_QueryService function](..\shlwapi\nf-shlwapi-iunknown_queryservice.md) | Retrieves an interface for a service from a specified object. |
| [IUnknown_Set function](..\shlwapi\nf-shlwapi-iunknown_set.md) | Changes the value of a Component Object Model (COM) interface pointer and releases the previous interface. |
| [IUnknown_SetSite function](..\shlwapi\nf-shlwapi-iunknown_setsite.md) | Sets the specified object's site by calling its IObjectWithSite |
| [InetIsOffline function](..\intshcut\nf-intshcut-inetisoffline.md) | Determines whether the system is connected to the Internet. |
| [Int8Add function](..\intsafe\nf-intsafe-int8add.md) | Adds two values of type INT8. |
| [Int8Mult function](..\intsafe\nf-intsafe-int8mult.md) | Multiplies two values of type INT8. |
| [Int8Sub function](..\intsafe\nf-intsafe-int8sub.md) | Subtracts one value of type INT8 from another. |
| [Int8ToUChar function](..\intsafe\nf-intsafe-int8touchar.md) | Converts a value of type INT8 to a value of type UCHAR. |
| [Int8ToUInt function](..\intsafe\nf-intsafe-int8touint.md) | Converts a value of type INT8 to a value of type UINT. |
| [Int8ToUInt8 function](..\intsafe\nf-intsafe-int8touint8.md) | Converts a value of type INT8 to a value of type UINT8. |
| [Int8ToUIntPtr function](..\intsafe\nf-intsafe-int8touintptr.md) | Converts a value of type INT8 to a value of type UINT_PTR. |
| [Int8ToULong function](..\intsafe\nf-intsafe-int8toulong.md) | Converts a value of type INT8 to a value of type ULONG. |
| [Int8ToULongLong function](..\intsafe\nf-intsafe-int8toulonglong.md) | Converts a value of type INT8 to a value of type ULONGLONG. |
| [Int8ToULongPtr function](..\intsafe\nf-intsafe-int8toulongptr.md) | Converts a value of type INT8 to a value of type ULONG_PTR. |
| [Int8ToUShort function](..\intsafe\nf-intsafe-int8toushort.md) | Converts a value of type INT8 to a value of type USHORT. |
| [IntAdd function](..\intsafe\nf-intsafe-intadd.md) | Adds two values of type INT. |
| [IntMult function](..\intsafe\nf-intsafe-intmult.md) | Multiplies two values of type INT. |
| [IntPtrAdd function](..\intsafe\nf-intsafe-intptradd.md) | Adds two values of type INT_PTR. |
| [IntPtrMult function](..\intsafe\nf-intsafe-intptrmult.md) | Multiplies two values of type INT_PTR. |
| [IntPtrSub function](..\intsafe\nf-intsafe-intptrsub.md) | Subtracts one value of type INT_PTR from another. |
| [IntPtrToChar function](..\intsafe\nf-intsafe-intptrtochar.md) | Converts a value of type INT_PTR to a value of type CHAR. |
| [IntPtrToInt function](..\intsafe\nf-intsafe-intptrtoint.md) | Converts a value of type INT_PTR to a value of type INT. |
| [IntPtrToInt8 function](..\intsafe\nf-intsafe-intptrtoint8.md) | Converts a value of type INT_PTR to a value of type INT8. |
| [IntPtrToLong function](..\intsafe\nf-intsafe-intptrtolong.md) | Converts a value of type INT_PTR to a value of type LONG. |
| [IntPtrToLongPtr function](..\intsafe\nf-intsafe-intptrtolongptr.md) | Converts a value of type INT_PTR to a value of type LONG_PTR. |
| [IntPtrToShort function](..\intsafe\nf-intsafe-intptrtoshort.md) | Converts a value of type INT_PTR to a value of type SHORT. |
| [IntPtrToUChar function](..\intsafe\nf-intsafe-intptrtouchar.md) | Converts a value of type INT_PTR to a value of type UCHAR. |
| [IntPtrToUInt function](..\intsafe\nf-intsafe-intptrtouint.md) | Converts a value of type INT_PTR to a value of type UINT. |
| [IntPtrToUInt8 function](..\intsafe\nf-intsafe-intptrtouint8.md) | Converts a value of type INT_PTR to a value of type UINT8. |
| [IntPtrToUIntPtr function](..\intsafe\nf-intsafe-intptrtouintptr.md) | Converts a value of type INT_PTR to a value of type size_t. |
| [IntPtrToULong function](..\intsafe\nf-intsafe-intptrtoulong.md) | Converts a value of type INT_PTR to a value of type DWORD. |
| [IntPtrToULongLong function](..\intsafe\nf-intsafe-intptrtoulonglong.md) | Converts a value of type INT_PTR to a value of type ULONGLONG. |
| [IntPtrToULongPtr function](..\intsafe\nf-intsafe-intptrtoulongptr.md) | Converts a value of type INT_PTR to a value of type DWORD_PTR. |
| [IntPtrToUShort function](..\intsafe\nf-intsafe-intptrtoushort.md) | Converts a value of type INT_PTR to a value of type USHORT. |
| [IntSub function](..\intsafe\nf-intsafe-intsub.md) | Subtracts one value of type INT from another. |
| [IntToChar function](..\intsafe\nf-intsafe-inttochar.md) | Converts a value of type INT to a value of type CHAR. |
| [IntToInt8 function](..\intsafe\nf-intsafe-inttoint8.md) | Converts a value of type INT to a value of type INT8. |
| [IntToShort function](..\intsafe\nf-intsafe-inttoshort.md) | Converts a value of type INT to a value of type SHORT. |
| [IntToUChar function](..\intsafe\nf-intsafe-inttouchar.md) | Converts a value of type INT to a value of type UCHAR. |
| [IntToUInt function](..\intsafe\nf-intsafe-inttouint.md) | Converts a value of type INT to a value of type UINT. |
| [IntToUInt8 function](..\intsafe\nf-intsafe-inttouint8.md) | Converts a value of type INT to a value of type BYTE. |
| [IntToULong function](..\intsafe\nf-intsafe-inttoulong.md) | Converts a value of type INT to a value of type DWORD. |
| [IntToULongLong function](..\intsafe\nf-intsafe-inttoulonglong.md) | Converts a value of type INT to a value of type UINT_PTR. |
| [IntToUShort function](..\intsafe\nf-intsafe-inttoushort.md) | Converts a value of type INT to a value of type USHORT. |
| [IntlStrEqWorkerA function](..\shlwapi\nf-shlwapi-intlstreqworkera.md) | Compares a specified number of characters from the beginning of two localized strings. |
| [IntlStrEqWorkerW function](..\shlwapi\nf-shlwapi-intlstreqworkerw.md) | Compares a specified number of characters from the beginning of two localized strings. |
| [IsCharSpaceA function](..\shlwapi\nf-shlwapi-ischarspacea.md) | Determines whether a character represents a space. |
| [IsCharSpaceW function](..\shlwapi\nf-shlwapi-ischarspacew.md) | Determines whether a character represents a space. |
| [IsInternetESCEnabled function](..\shlwapi\nf-shlwapi-isinternetescenabled.md) | Determines whether Windows Internet Explorer is in the Enhanced Security Configuration. |
| [IsNetDrive function](..\shlobj_core\nf-shlobj_core-isnetdrive.md) | Tests whether a drive is a network drive. |
| [IsOS function](..\shlwapi\nf-shlwapi-isos.md) | Checks for specified operating systems and operating system features. |
| [IsUserAnAdmin function](..\shlobj_core\nf-shlobj_core-isuseranadmin.md) | IsUserAnAdmin may be altered or unavailable. |
| [LoadUserProfileA function](..\userenv\nf-userenv-loaduserprofilea.md) | Loads the specified user's profile. The profile can be a local user profile or a roaming user profile. |
| [LoadUserProfileW function](..\userenv\nf-userenv-loaduserprofilew.md) | Loads the specified user's profile. The profile can be a local user profile or a roaming user profile. |
| [LongAdd function](..\intsafe\nf-intsafe-longadd.md) | Adds two values of type LONG. |
| [LongLongAdd function](..\intsafe\nf-intsafe-longlongadd.md) | Adds two values of type LONGLONG. |
| [LongLongMult function](..\intsafe\nf-intsafe-longlongmult.md) | Multiplies two values of type LONGLONG. |
| [LongLongSub function](..\intsafe\nf-intsafe-longlongsub.md) | Subtracts one value of type LONGLONG from another. |
| [LongLongToChar function](..\intsafe\nf-intsafe-longlongtochar.md) | Converts a value of type LONGLONG to a value of type CHAR. |
| [LongLongToInt function](..\intsafe\nf-intsafe-longlongtoint.md) | Converts a value of type INT64 to a value of type INT. |
| [LongLongToInt8 function](..\intsafe\nf-intsafe-longlongtoint8.md) | Converts a value of type LONGLONG to a value of type INT8. |
| [LongLongToIntPtr function](..\intsafe\nf-intsafe-longlongtointptr.md) | Converts a value of type INT64 to a value of type INT_PTR. |
| [LongLongToLong function](..\intsafe\nf-intsafe-longlongtolong.md) | Converts a value of type INT64 to a value of type LONG. |
| [LongLongToLongPtr function](..\intsafe\nf-intsafe-longlongtolongptr.md) | Converts a value of type INT64 to a value of type LONG_PTR. |
| [LongLongToShort function](..\intsafe\nf-intsafe-longlongtoshort.md) | Converts a value of type LONGLONG to a value of type SHORT. |
| [LongLongToUChar function](..\intsafe\nf-intsafe-longlongtouchar.md) | Converts a value of type LONGLONG to a value of type UCHAR. |
| [LongLongToUInt function](..\intsafe\nf-intsafe-longlongtouint.md) | Converts a value of type LONGLONG to a value of type UINT. |
| [LongLongToUInt8 function](..\intsafe\nf-intsafe-longlongtouint8.md) | Converts a value of type LONGLONG to a value of type UINT8. |
| [LongLongToULong function](..\intsafe\nf-intsafe-longlongtoulong.md) | Converts a value of type DWORD to a value of type USHORT. |
| [LongLongToULongLong function](..\intsafe\nf-intsafe-longlongtoulonglong.md) | Converts a value of type INT64 to a value of type ULONGLONG. |
| [LongLongToUShort function](..\intsafe\nf-intsafe-longlongtoushort.md) | Converts a value of type LONGLONG to a value of type USHORT. |
| [LongMult function](..\intsafe\nf-intsafe-longmult.md) | Multiplies two values of type LONG. |
| [LongPtrAdd function](..\intsafe\nf-intsafe-longptradd.md) | Adds two values of type LONG_PTR. |
| [LongPtrMult function](..\intsafe\nf-intsafe-longptrmult.md) | Multiplies two values of type LONG_PTR. |
| [LongPtrSub function](..\intsafe\nf-intsafe-longptrsub.md) | Subtracts one value of type LONG_PTR from another. |
| [LongPtrToChar function](..\intsafe\nf-intsafe-longptrtochar.md) | Converts a value of type LONG_PTR to a value of type CHAR. |
| [LongPtrToInt function](..\intsafe\nf-intsafe-longptrtoint.md) | Converts a value of type LONG_PTR to a value of type INT. |
| [LongPtrToInt8 function](..\intsafe\nf-intsafe-longptrtoint8.md) | Converts a value of type LONG_PTR to a value of type INT8. |
| [LongPtrToIntPtr function](..\intsafe\nf-intsafe-longptrtointptr.md) | Converts a value of type LONG_PTR to a value of type INT_PTR. |
| [LongPtrToLong function](..\intsafe\nf-intsafe-longptrtolong.md) | Converts a value of type LONG_PTR to a value of type LONG. |
| [LongPtrToShort function](..\intsafe\nf-intsafe-longptrtoshort.md) | Converts a value of type LONG_PTR to a value of type SHORT. |
| [LongPtrToUChar function](..\intsafe\nf-intsafe-longptrtouchar.md) | Converts a value of type LONG_PTR to a value of type UCHAR. |
| [LongPtrToUInt function](..\intsafe\nf-intsafe-longptrtouint.md) | Converts a value of type LONG_PTR to a value of type UINT. |
| [LongPtrToUInt8 function](..\intsafe\nf-intsafe-longptrtouint8.md) | Converts a value of type LONG_PTR to a value of type UINT8. |
| [LongPtrToUIntPtr function](..\intsafe\nf-intsafe-longptrtouintptr.md) | Converts a value of type LONG_PTR to a value of type UINT_PTR. |
| [LongPtrToULong function](..\intsafe\nf-intsafe-longptrtoulong.md) | Converts a value of type LONG_PTR to a value of type DWORD. |
| [LongPtrToULongLong function](..\intsafe\nf-intsafe-longptrtoulonglong.md) | Converts a value of type LONG_PTR to a value of type ULONGLONG. |
| [LongPtrToULongPtr function](..\intsafe\nf-intsafe-longptrtoulongptr.md) | Converts a value of type LONG_PTR to a value of type DWORD_PTR. |
| [LongPtrToUShort function](..\intsafe\nf-intsafe-longptrtoushort.md) | Converts a value of type LONG_PTR to a value of type USHORT. |
| [LongSub function](..\intsafe\nf-intsafe-longsub.md) | Subtracts one value of type LONG from another. |
| [LongToChar function](..\intsafe\nf-intsafe-longtochar.md) | Converts a value of type LONG to a value of type CHAR. |
| [LongToInt function](..\intsafe\nf-intsafe-longtoint.md) | Converts a value of type LONG to a value of type INT. |
| [LongToInt8 function](..\intsafe\nf-intsafe-longtoint8.md) | Converts a value of type LONG to a value of type INT8. |
| [LongToIntPtr function](..\intsafe\nf-intsafe-longtointptr.md) | Converts a value of type LONG to a value of type INT_PTR. |
| [LongToShort function](..\intsafe\nf-intsafe-longtoshort.md) | Converts a value of type LONG to a value of type SHORT. |
| [LongToUChar function](..\intsafe\nf-intsafe-longtouchar.md) | Converts a value of type LONG to a value of type UCHAR. |
| [LongToUInt function](..\intsafe\nf-intsafe-longtouint.md) | Converts a value of type LONG to a value of type UINT. |
| [LongToUInt8 function](..\intsafe\nf-intsafe-longtouint8.md) | Converts a value of type LONG to a value of type BYTE. |
| [LongToUIntPtr function](..\intsafe\nf-intsafe-longtouintptr.md) | Converts a value of type LONG to a value of type size_t. |
| [LongToULong function](..\intsafe\nf-intsafe-longtoulong.md) | Converts a value of type LONG to a value of type DWORD. |
| [LongToULongLong function](..\intsafe\nf-intsafe-longtoulonglong.md) | Converts a value of type LONG to a value of type ULONGLONG. |
| [LongToULongPtr function](..\intsafe\nf-intsafe-longtoulongptr.md) | Converts a value of type LONG to a value of type ULONG_PTR. |
| [LongToUShort function](..\intsafe\nf-intsafe-longtoushort.md) | Converts a value of type LONG to a value of type USHORT. |
| [MIMEAssociationDialogA function](..\intshcut\nf-intshcut-mimeassociationdialoga.md) | Runs the unregistered MIME content type dialog box.Note  Windows XP Service Pack 2 (SP2) or later |
| [MIMEAssociationDialogW function](..\intshcut\nf-intshcut-mimeassociationdialogw.md) | Runs the unregistered MIME content type dialog box.Note  Windows XP Service Pack 2 (SP2) or later |
| [OpenRegStream function](..\shlobj_core\nf-shlobj_core-openregstream.md) | OpenRegStream may be altered or unavailable. Instead, use SHOpenRegStream2 or SHOpenRegStream. |
| [ParseURLA function](..\shlwapi\nf-shlwapi-parseurla.md) | Performs rudimentary parsing of a URL. |
| [ParseURLW function](..\shlwapi\nf-shlwapi-parseurlw.md) | Performs rudimentary parsing of a URL. |
| [PathAddBackslashA function](..\shlwapi\nf-shlwapi-pathaddbackslasha.md) | Adds a backslash to the end of a string to create the correct syntax for a path. |
| [PathAddBackslashW function](..\shlwapi\nf-shlwapi-pathaddbackslashw.md) | Adds a backslash to the end of a string to create the correct syntax for a path. |
| [PathAddExtensionA function](..\shlwapi\nf-shlwapi-pathaddextensiona.md) | Adds a file name extension to a path string. |
| [PathAddExtensionW function](..\shlwapi\nf-shlwapi-pathaddextensionw.md) | Adds a file name extension to a path string. |
| [PathAllocCanonicalize function](..\pathcch\nf-pathcch-pathalloccanonicalize.md) | Converts a path string into a canonical form.This function differs from PathCchCanonicalize and PathCchCanonicalizeEx in that it returns the result on the heap. |
| [PathAllocCombine function](..\pathcch\nf-pathcch-pathalloccombine.md) | Concatenates two path fragments into a single path. |
| [PathAppendA function](..\shlwapi\nf-shlwapi-pathappenda.md) | Appends one path to the end of another. |
| [PathAppendW function](..\shlwapi\nf-shlwapi-pathappendw.md) | Appends one path to the end of another. |
| [PathBuildRootA function](..\shlwapi\nf-shlwapi-pathbuildroota.md) | Creates a root path from a given drive number. |
| [PathBuildRootW function](..\shlwapi\nf-shlwapi-pathbuildrootw.md) | Creates a root path from a given drive number. |
| [PathCanonicalizeA function](..\shlwapi\nf-shlwapi-pathcanonicalizea.md) | Simplifies a path by removing navigation elements such as &#0034;.&#0034; and &#0034;..&#0034; to produce a direct, well-formed path. |
| [PathCanonicalizeW function](..\shlwapi\nf-shlwapi-pathcanonicalizew.md) | Simplifies a path by removing navigation elements such as &#0034;.&#0034; and &#0034;..&#0034; to produce a direct, well-formed path. |
| [PathCchAddBackslash function](..\pathcch\nf-pathcch-pathcchaddbackslash.md) | Adds a backslash to the end of a string to create the correct syntax for a path. |
| [PathCchAddBackslashEx function](..\pathcch\nf-pathcch-pathcchaddbackslashex.md) | Adds a backslash to the end of a string to create the correct syntax for a path. |
| [PathCchAddExtension function](..\pathcch\nf-pathcch-pathcchaddextension.md) | Adds a file name extension to a path string.This function differs from PathAddExtension in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchAppend function](..\pathcch\nf-pathcch-pathcchappend.md) | Appends one path to the end of another.This function differs from PathCchAppendEx in that you are restricted to a final path of length MAX_PATH.This function differs from PathAppend in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchAppendEx function](..\pathcch\nf-pathcch-pathcchappendex.md) | Appends one path to the end of another.This function differs from PathCchAppend in that it allows for a longer final path to be constructed.This function differs from PathAppend in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchCanonicalize function](..\pathcch\nf-pathcch-pathcchcanonicalize.md) | Converts a path string into a canonical form.This function differs from PathCchCanonicalizeEx in that you are restricted to a final path of length MAX_PATH.This function differs from PathAllocCanonicalize in that the caller must declare the size of the returned string, which is stored on the stack.This function differs from PathCanonicalize in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchCanonicalizeEx function](..\pathcch\nf-pathcch-pathcchcanonicalizeex.md) | Simplifies a path by removing navigation elements such as &#0034;.&#0034; and &#0034;..&#0034; to produce a direct, well-formed path.This function differs from PathCchCanonicalize in that it allows for a longer final path to be constructed.This function differs from PathAllocCanonicalize in that the caller must declare the size of the returned string, which is stored on the stack.This function differs from PathCanonicalize in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchCombine function](..\pathcch\nf-pathcch-pathcchcombine.md) | Combines two path fragments into a single path. |
| [PathCchCombineEx function](..\pathcch\nf-pathcch-pathcchcombineex.md) | Combines two path fragments into a single path. |
| [PathCchFindExtension function](..\pathcch\nf-pathcch-pathcchfindextension.md) | Searches a path to find its file name extension, such as &#0034;.exe&#0034; or &#0034;.ini&#0034;. |
| [PathCchIsRoot function](..\pathcch\nf-pathcch-pathcchisroot.md) | Determines whether a path string refers to the root of a volume.This function differs from PathIsRoot in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchRemoveBackslash function](..\pathcch\nf-pathcch-pathcchremovebackslash.md) | Removes the trailing backslash from the end of a path string.This function differs from PathRemoveBackslash in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchRemoveBackslashEx function](..\pathcch\nf-pathcch-pathcchremovebackslashex.md) | Removes the trailing backslash from the end of a path string.This function differs from PathCchRemoveBackslash in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.This function differs from PathRemoveBackslash in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchRemoveExtension function](..\pathcch\nf-pathcch-pathcchremoveextension.md) | Removes the file name extension from a path, if one is present.This function differs from PathRemoveExtension in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchRemoveFileSpec function](..\pathcch\nf-pathcch-pathcchremovefilespec.md) | Removes the last element in a path string, whether that element is a file name or a directory name. |
| [PathCchRenameExtension function](..\pathcch\nf-pathcch-pathcchrenameextension.md) | Replaces a file name's extension at the end of a path string with a new extension. |
| [PathCchSkipRoot function](..\pathcch\nf-pathcch-pathcchskiproot.md) | Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.This function differs from PathSkipRoot in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCchStripPrefix function](..\pathcch\nf-pathcch-pathcchstripprefix.md) | Removes the &#0034;\\?\&#0034; prefix, if present, from a file path. |
| [PathCchStripToRoot function](..\pathcch\nf-pathcch-pathcchstriptoroot.md) | Removes all file and directory elements in a path except for the root information.This function differs from PathStripToRoot in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes. |
| [PathCleanupSpec function](..\shlobj_core\nf-shlobj_core-pathcleanupspec.md) | PathCleanupSpec may be altered or unavailable. |
| [PathCombineA function](..\shlwapi\nf-shlwapi-pathcombinea.md) | Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements. |
| [PathCombineW function](..\shlwapi\nf-shlwapi-pathcombinew.md) | Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements. |
| [PathCommonPrefixA function](..\shlwapi\nf-shlwapi-pathcommonprefixa.md) | Compares two paths to determine if they share a common prefix. A prefix is one of these types |
| [PathCommonPrefixW function](..\shlwapi\nf-shlwapi-pathcommonprefixw.md) | Compares two paths to determine if they share a common prefix. A prefix is one of these types |
| [PathCompactPathA function](..\shlwapi\nf-shlwapi-pathcompactpatha.md) | Truncates a file path to fit within a given pixel width by replacing path components with ellipses. |
| [PathCompactPathExA function](..\shlwapi\nf-shlwapi-pathcompactpathexa.md) | Truncates a path to fit within a certain number of characters by replacing path components with ellipses. |
| [PathCompactPathExW function](..\shlwapi\nf-shlwapi-pathcompactpathexw.md) | Truncates a path to fit within a certain number of characters by replacing path components with ellipses. |
| [PathCompactPathW function](..\shlwapi\nf-shlwapi-pathcompactpathw.md) | Truncates a file path to fit within a given pixel width by replacing path components with ellipses. |
| [PathCreateFromUrlA function](..\shlwapi\nf-shlwapi-pathcreatefromurla.md) | Converts a file URL to a Microsoft MS-DOS path. |
| [PathCreateFromUrlAlloc function](..\shlwapi\nf-shlwapi-pathcreatefromurlalloc.md) | Creates a path from a file URL. |
| [PathCreateFromUrlW function](..\shlwapi\nf-shlwapi-pathcreatefromurlw.md) | Converts a file URL to a Microsoft MS-DOS path. |
| [PathFileExistsA function](..\shlwapi\nf-shlwapi-pathfileexistsa.md) | Determines whether a path to a file system object such as a file or folder is valid. |
| [PathFileExistsW function](..\shlwapi\nf-shlwapi-pathfileexistsw.md) | Determines whether a path to a file system object such as a file or folder is valid. |
| [PathFindExtensionA function](..\shlwapi\nf-shlwapi-pathfindextensiona.md) | Searches a path for an extension. |
| [PathFindExtensionW function](..\shlwapi\nf-shlwapi-pathfindextensionw.md) | Searches a path for an extension. |
| [PathFindFileNameA function](..\shlwapi\nf-shlwapi-pathfindfilenamea.md) | Searches a path for a file name. |
| [PathFindFileNameW function](..\shlwapi\nf-shlwapi-pathfindfilenamew.md) | Searches a path for a file name. |
| [PathFindNextComponentA function](..\shlwapi\nf-shlwapi-pathfindnextcomponenta.md) | Parses a path and returns the portion of that path that follows the first backslash. |
| [PathFindNextComponentW function](..\shlwapi\nf-shlwapi-pathfindnextcomponentw.md) | Parses a path and returns the portion of that path that follows the first backslash. |
| [PathFindOnPathA function](..\shlwapi\nf-shlwapi-pathfindonpatha.md) | Searches for a file. |
| [PathFindOnPathW function](..\shlwapi\nf-shlwapi-pathfindonpathw.md) | Searches for a file. |
| [PathFindSuffixArrayA function](..\shlwapi\nf-shlwapi-pathfindsuffixarraya.md) | Determines whether a given file name has one of a list of suffixes. |
| [PathFindSuffixArrayW function](..\shlwapi\nf-shlwapi-pathfindsuffixarrayw.md) | Determines whether a given file name has one of a list of suffixes. |
| [PathGetArgsA function](..\shlwapi\nf-shlwapi-pathgetargsa.md) | Finds the command line arguments within a given path. |
| [PathGetArgsW function](..\shlwapi\nf-shlwapi-pathgetargsw.md) | Finds the command line arguments within a given path. |
| [PathGetCharTypeA function](..\shlwapi\nf-shlwapi-pathgetchartypea.md) | Determines the type of character in relation to a path. |
| [PathGetCharTypeW function](..\shlwapi\nf-shlwapi-pathgetchartypew.md) | Determines the type of character in relation to a path. |
| [PathGetDriveNumberA function](..\shlwapi\nf-shlwapi-pathgetdrivenumbera.md) | Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number. |
| [PathGetDriveNumberW function](..\shlwapi\nf-shlwapi-pathgetdrivenumberw.md) | Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number. |
| [PathGetShortPath function](..\shlobj_core\nf-shlobj_core-pathgetshortpath.md) | PathGetShortPath may be altered or unavailable. |
| [PathIsContentTypeA function](..\shlwapi\nf-shlwapi-pathiscontenttypea.md) | Determines if a file's registered content type matches the specified content type. This function obtains the content type for the specified file type and compares that string with the pszContentType. The comparison is not case-sensitive. |
| [PathIsContentTypeW function](..\shlwapi\nf-shlwapi-pathiscontenttypew.md) | Determines if a file's registered content type matches the specified content type. This function obtains the content type for the specified file type and compares that string with the pszContentType. The comparison is not case-sensitive. |
| [PathIsDirectoryA function](..\shlwapi\nf-shlwapi-pathisdirectorya.md) | Verifies that a path is a valid directory. |
| [PathIsDirectoryEmptyA function](..\shlwapi\nf-shlwapi-pathisdirectoryemptya.md) | Determines whether a specified path is an empty directory. |
| [PathIsDirectoryEmptyW function](..\shlwapi\nf-shlwapi-pathisdirectoryemptyw.md) | Determines whether a specified path is an empty directory. |
| [PathIsDirectoryW function](..\shlwapi\nf-shlwapi-pathisdirectoryw.md) | Verifies that a path is a valid directory. |
| [PathIsExe function](..\shlobj_core\nf-shlobj_core-pathisexe.md) | PathIsExe may be altered or unavailable. |
| [PathIsFileSpecA function](..\shlwapi\nf-shlwapi-pathisfilespeca.md) | Searches a path for any path-delimiting characters (for example, ' |
| [PathIsFileSpecW function](..\shlwapi\nf-shlwapi-pathisfilespecw.md) | Searches a path for any path-delimiting characters (for example, ' |
| [PathIsLFNFileSpecA function](..\shlwapi\nf-shlwapi-pathislfnfilespeca.md) | Determines whether a file name is in long format. |
| [PathIsLFNFileSpecW function](..\shlwapi\nf-shlwapi-pathislfnfilespecw.md) | Determines whether a file name is in long format. |
| [PathIsNetworkPathA function](..\shlwapi\nf-shlwapi-pathisnetworkpatha.md) | Determines whether a path string represents a network resource. |
| [PathIsNetworkPathW function](..\shlwapi\nf-shlwapi-pathisnetworkpathw.md) | Determines whether a path string represents a network resource. |
| [PathIsPrefixA function](..\shlwapi\nf-shlwapi-pathisprefixa.md) | Searches a path to determine if it contains a valid prefix of the type passed by pszPrefix. A prefix is one of these types |
| [PathIsPrefixW function](..\shlwapi\nf-shlwapi-pathisprefixw.md) | Searches a path to determine if it contains a valid prefix of the type passed by pszPrefix. A prefix is one of these types |
| [PathIsRelativeA function](..\shlwapi\nf-shlwapi-pathisrelativea.md) | Searches a path and determines if it is relative. |
| [PathIsRelativeW function](..\shlwapi\nf-shlwapi-pathisrelativew.md) | Searches a path and determines if it is relative. |
| [PathIsRootA function](..\shlwapi\nf-shlwapi-pathisroota.md) | Determines whether a path string refers to the root of a volume. |
| [PathIsRootW function](..\shlwapi\nf-shlwapi-pathisrootw.md) | Determines whether a path string refers to the root of a volume. |
| [PathIsSameRootA function](..\shlwapi\nf-shlwapi-pathissameroota.md) | Compares two paths to determine if they have a common root component. |
| [PathIsSameRootW function](..\shlwapi\nf-shlwapi-pathissamerootw.md) | Compares two paths to determine if they have a common root component. |
| [PathIsSystemFolderA function](..\shlwapi\nf-shlwapi-pathissystemfoldera.md) | Determines if an existing folder contains the attributes that make it a system folder. Alternately, this function indicates if certain attributes qualify a folder to be a system folder. |
| [PathIsSystemFolderW function](..\shlwapi\nf-shlwapi-pathissystemfolderw.md) | Determines if an existing folder contains the attributes that make it a system folder. Alternately, this function indicates if certain attributes qualify a folder to be a system folder. |
| [PathIsUNCA function](..\shlwapi\nf-shlwapi-pathisunca.md) | Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter. |
| [PathIsUNCEx function](..\pathcch\nf-pathcch-pathisuncex.md) | Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.This function differs from PathIsUNC in that it also allows you to extract the name of the server from the path. |
| [PathIsUNCServerA function](..\shlwapi\nf-shlwapi-pathisuncservera.md) | Determines if a string is a valid Universal Naming Convention (UNC) for a server path only. |
| [PathIsUNCServerShareA function](..\shlwapi\nf-shlwapi-pathisuncserversharea.md) | Determines if a string is a valid Universal Naming Convention (UNC) share path, \\server\share. |
| [PathIsUNCServerShareW function](..\shlwapi\nf-shlwapi-pathisuncserversharew.md) | Determines if a string is a valid Universal Naming Convention (UNC) share path, \\server\share. |
| [PathIsUNCServerW function](..\shlwapi\nf-shlwapi-pathisuncserverw.md) | Determines if a string is a valid Universal Naming Convention (UNC) for a server path only. |
| [PathIsUNCW function](..\shlwapi\nf-shlwapi-pathisuncw.md) | Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter. |
| [PathIsURLA function](..\shlwapi\nf-shlwapi-pathisurla.md) | Tests a given string to determine if it conforms to a valid URL format. |
| [PathIsURLW function](..\shlwapi\nf-shlwapi-pathisurlw.md) | Tests a given string to determine if it conforms to a valid URL format. |
| [PathMakePrettyA function](..\shlwapi\nf-shlwapi-pathmakeprettya.md) | Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance. |
| [PathMakePrettyW function](..\shlwapi\nf-shlwapi-pathmakeprettyw.md) | Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance. |
| [PathMakeSystemFolderA function](..\shlwapi\nf-shlwapi-pathmakesystemfoldera.md) | Gives an existing folder the proper attributes to become a system folder. |
| [PathMakeSystemFolderW function](..\shlwapi\nf-shlwapi-pathmakesystemfolderw.md) | Gives an existing folder the proper attributes to become a system folder. |
| [PathMakeUniqueName function](..\shlobj_core\nf-shlobj_core-pathmakeuniquename.md) | Creates a unique path name from a template. |
| [PathMatchSpecA function](..\shlwapi\nf-shlwapi-pathmatchspeca.md) | Searches a string using a Microsoft MS-DOS wildcard match type. |
| [PathMatchSpecExA function](..\shlwapi\nf-shlwapi-pathmatchspecexa.md) | Matches a file name from a path against one or more file name patterns. |
| [PathMatchSpecExW function](..\shlwapi\nf-shlwapi-pathmatchspecexw.md) | Matches a file name from a path against one or more file name patterns. |
| [PathMatchSpecW function](..\shlwapi\nf-shlwapi-pathmatchspecw.md) | Searches a string using a Microsoft MS-DOS wildcard match type. |
| [PathParseIconLocationA function](..\shlwapi\nf-shlwapi-pathparseiconlocationa.md) | Parses a file location string that contains a file location and icon index, and returns separate values. |
| [PathParseIconLocationW function](..\shlwapi\nf-shlwapi-pathparseiconlocationw.md) | Parses a file location string that contains a file location and icon index, and returns separate values. |
| [PathQuoteSpacesA function](..\shlwapi\nf-shlwapi-pathquotespacesa.md) | Searches a path for spaces. If spaces are found, the entire path is enclosed in quotation marks. |
| [PathQuoteSpacesW function](..\shlwapi\nf-shlwapi-pathquotespacesw.md) | Searches a path for spaces. If spaces are found, the entire path is enclosed in quotation marks. |
| [PathRelativePathToA function](..\shlwapi\nf-shlwapi-pathrelativepathtoa.md) | Creates a relative path from one file or folder to another. |
| [PathRelativePathToW function](..\shlwapi\nf-shlwapi-pathrelativepathtow.md) | Creates a relative path from one file or folder to another. |
| [PathRemoveArgsA function](..\shlwapi\nf-shlwapi-pathremoveargsa.md) | Removes any arguments from a given path. |
| [PathRemoveArgsW function](..\shlwapi\nf-shlwapi-pathremoveargsw.md) | Removes any arguments from a given path. |
| [PathRemoveBackslashA function](..\shlwapi\nf-shlwapi-pathremovebackslasha.md) | Removes the trailing backslash from a given path. |
| [PathRemoveBackslashW function](..\shlwapi\nf-shlwapi-pathremovebackslashw.md) | Removes the trailing backslash from a given path. |
| [PathRemoveBlanksA function](..\shlwapi\nf-shlwapi-pathremoveblanksa.md) | Removes all leading and trailing spaces from a string. |
| [PathRemoveBlanksW function](..\shlwapi\nf-shlwapi-pathremoveblanksw.md) | Removes all leading and trailing spaces from a string. |
| [PathRemoveExtensionA function](..\shlwapi\nf-shlwapi-pathremoveextensiona.md) | Removes the file name extension from a path, if one is present. |
| [PathRemoveExtensionW function](..\shlwapi\nf-shlwapi-pathremoveextensionw.md) | Removes the file name extension from a path, if one is present. |
| [PathRemoveFileSpecA function](..\shlwapi\nf-shlwapi-pathremovefilespeca.md) | Removes the trailing file name and backslash from a path, if they are present. |
| [PathRemoveFileSpecW function](..\shlwapi\nf-shlwapi-pathremovefilespecw.md) | Removes the trailing file name and backslash from a path, if they are present. |
| [PathRenameExtensionA function](..\shlwapi\nf-shlwapi-pathrenameextensiona.md) | Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string. |
| [PathRenameExtensionW function](..\shlwapi\nf-shlwapi-pathrenameextensionw.md) | Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string. |
| [PathResolve function](..\shlobj_core\nf-shlobj_core-pathresolve.md) | PathResolve may be altered or unavailable. |
| [PathSearchAndQualifyA function](..\shlwapi\nf-shlwapi-pathsearchandqualifya.md) | Determines if a given path is correctly formatted and fully qualified. |
| [PathSearchAndQualifyW function](..\shlwapi\nf-shlwapi-pathsearchandqualifyw.md) | Determines if a given path is correctly formatted and fully qualified. |
| [PathSetDlgItemPathA function](..\shlwapi\nf-shlwapi-pathsetdlgitempatha.md) | Sets the text of a child control in a window or dialog box, using PathCompactPath to ensure the path fits in the control. |
| [PathSetDlgItemPathW function](..\shlwapi\nf-shlwapi-pathsetdlgitempathw.md) | Sets the text of a child control in a window or dialog box, using PathCompactPath to ensure the path fits in the control. |
| [PathSkipRootA function](..\shlwapi\nf-shlwapi-pathskiproota.md) | Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements. |
| [PathSkipRootW function](..\shlwapi\nf-shlwapi-pathskiprootw.md) | Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements. |
| [PathStripPathA function](..\shlwapi\nf-shlwapi-pathstrippatha.md) | Removes the path portion of a fully qualified path and file. |
| [PathStripPathW function](..\shlwapi\nf-shlwapi-pathstrippathw.md) | Removes the path portion of a fully qualified path and file. |
| [PathStripToRootA function](..\shlwapi\nf-shlwapi-pathstriptoroota.md) | Removes all file and directory elements in a path except for the root information. |
| [PathStripToRootW function](..\shlwapi\nf-shlwapi-pathstriptorootw.md) | Removes all file and directory elements in a path except for the root information. |
| [PathUnExpandEnvStringsA function](..\shlwapi\nf-shlwapi-pathunexpandenvstringsa.md) | Replaces certain folder names in a fully qualified path with their associated environment string. |
| [PathUnExpandEnvStringsW function](..\shlwapi\nf-shlwapi-pathunexpandenvstringsw.md) | Replaces certain folder names in a fully qualified path with their associated environment string. |
| [PathUndecorateA function](..\shlwapi\nf-shlwapi-pathundecoratea.md) | Removes the decoration from a path string. |
| [PathUndecorateW function](..\shlwapi\nf-shlwapi-pathundecoratew.md) | Removes the decoration from a path string. |
| [PathUnmakeSystemFolderA function](..\shlwapi\nf-shlwapi-pathunmakesystemfoldera.md) | Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system. |
| [PathUnmakeSystemFolderW function](..\shlwapi\nf-shlwapi-pathunmakesystemfolderw.md) | Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system. |
| [PathUnquoteSpacesA function](..\shlwapi\nf-shlwapi-pathunquotespacesa.md) | Removes quotes from the beginning and end of a path. |
| [PathUnquoteSpacesW function](..\shlwapi\nf-shlwapi-pathunquotespacesw.md) | Removes quotes from the beginning and end of a path. |
| [PathYetAnotherMakeUniqueName function](..\shlobj_core\nf-shlobj_core-pathyetanothermakeuniquename.md) | Creates a unique filename based on an existing filename. |
| [PickIconDlg function](..\shlobj_core\nf-shlobj_core-pickicondlg.md) | PickIconDlg may be altered or unavailable. |
| [PtrdiffTAdd function](..\intsafe\nf-intsafe-ptrdifftadd.md) | Adds two values of type ptrdiff_t. |
| [PtrdiffTMult function](..\intsafe\nf-intsafe-ptrdifftmult.md) | Multiplies two values of type ptrdiff_t. |
| [PtrdiffTSub function](..\intsafe\nf-intsafe-ptrdifftsub.md) | Subtracts one value of type ptrdiff_t from another. |
| [QISearch function](..\shlwapi\nf-shlwapi-qisearch.md) | A table-driven implementation of the IUnknown |
| [ReadCabinetState function](..\shlobj_core\nf-shlobj_core-readcabinetstate.md) | ReadCabinetState may be altered or unavailable. |
| [RealDriveType function](..\shlobj_core\nf-shlobj_core-realdrivetype.md) | RealDriveType may be altered or unavailable. |
| [RegisterAppStateChangeNotification function](..\appnotify\nf-appnotify-registerappstatechangenotification.md) | Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state. |
| [RegisterDialogClasses function](..\scrnsave\nf-scrnsave-registerdialogclasses.md) | Registers any nonstandard window classes required by a screen saver's configuration dialog box. |
| [RestartDialog function](..\shlobj_core\nf-shlobj_core-restartdialog.md) | Displays a dialog box that prompts the user to restart Windows. When the user clicks the button, the function calls ExitWindowsEx to attempt to restart Windows. |
| [RestartDialogEx function](..\shlobj_core\nf-shlobj_core-restartdialogex.md) | Displays a dialog box that asks the user to restart Windows. When the user clicks the button, the function calls ExitWindowsEx to attempt to restart Windows. |
| [SHAddFromPropSheetExtArray function](..\shlobj_core\nf-shlobj_core-shaddfrompropsheetextarray.md) | Adds pages to a property sheet extension array created by SHCreatePropSheetExtArray. |
| [SHAddToRecentDocs function](..\shlobj_core\nf-shlobj_core-shaddtorecentdocs.md) | Notifies the system that an item has been accessed, for the purposes of tracking those items used most recently and most frequently. This function can also be used to clear all usage data. |
| [SHAlloc function](..\shlobj_core\nf-shlobj_core-shalloc.md) | Allocates memory from the Shell's heap. |
| [SHAllocShared function](..\shlwapi\nf-shlwapi-shallocshared.md) | SHAllocShared may be altered or unavailable. |
| [SHAnsiToAnsi function](..\shlwapi\nf-shlwapi-shansitoansi.md) | Copies an ANSI string. |
| [SHAnsiToUnicode function](..\shlwapi\nf-shlwapi-shansitounicode.md) | Converts a string from the ANSI code page to the Unicode code page. |
| [SHAutoComplete function](..\shlwapi\nf-shlwapi-shautocomplete.md) | Instructs system edit controls to use AutoComplete to help complete URLs or file system paths. |
| [SHBindToFolderIDListParent function](..\shlobj_core\nf-shlobj_core-shbindtofolderidlistparent.md) | Given a Shell namespace item specified in the form of a folder, and an item identifier list relative to that folder, this function binds to the parent of the namespace item and optionally returns a pointer to the final component of the item identifier list. |
| [SHBindToFolderIDListParentEx function](..\shlobj_core\nf-shlobj_core-shbindtofolderidlistparentex.md) | Extends the SHBindToFolderIDListParent function by allowing the caller to specify a bind context. |
| [SHBindToObject function](..\shlobj_core\nf-shlobj_core-shbindtoobject.md) | Retrieves and binds to a specified object by using the Shell namespace IShellFolder |
| [SHBindToParent function](..\shlobj_core\nf-shlobj_core-shbindtoparent.md) | Takes a pointer to a fully qualified item identifier list (PIDL), and returns a specified interface pointer on the parent object. |
| [SHBrowseForFolderA function](..\shlobj_core\nf-shlobj_core-shbrowseforfoldera.md) | Displays a dialog box that enables the user to select a Shell folder. |
| [SHBrowseForFolderW function](..\shlobj_core\nf-shlobj_core-shbrowseforfolderw.md) | Displays a dialog box that enables the user to select a Shell folder. |
| [SHCLSIDFromString function](..\shlobj_core\nf-shlobj_core-shclsidfromstring.md) | Takes the string form of a class identifier (CLSID) and creates the corresponding CLSID. |
| [SHChangeNotification_Lock function](..\shlobj_core\nf-shlobj_core-shchangenotification_lock.md) | Locks the shared memory associated with a Shell change notification event. |
| [SHChangeNotification_Unlock function](..\shlobj_core\nf-shlobj_core-shchangenotification_unlock.md) | Unlocks shared memory for a change notification. |
| [SHChangeNotify function](..\shlobj_core\nf-shlobj_core-shchangenotify.md) | Notifies the system of an event that an application has performed. An application should use this function if it performs an action that may affect the Shell. |
| [SHChangeNotifyDeregister function](..\shlobj_core\nf-shlobj_core-shchangenotifyderegister.md) | Unregisters the client's window process from receiving SHChangeNotify messages. |
| [SHChangeNotifyRegister function](..\shlobj_core\nf-shlobj_core-shchangenotifyregister.md) | Registers a window to receive notifications from the file system or Shell, if the file system supports notifications. |
| [SHCloneSpecialIDList function](..\shlobj_core\nf-shlobj_core-shclonespecialidlist.md) | SHCloneSpecialIDList may be altered or unavailable. Instead, use SHGetSpecialFolderLocation. |
| [SHCoCreateInstance function](..\shlobj_core\nf-shlobj_core-shcocreateinstance.md) | SHCoCreateInstance may be altered or unavailable. Instead, use CoCreateInstance. |
| [SHCopyKeyA function](..\shlwapi\nf-shlwapi-shcopykeya.md) | Recursively copies the subkeys and values of the source subkey to the destination key. SHCopyKey does not copy the security attributes of the keys. |
| [SHCopyKeyW function](..\shlwapi\nf-shlwapi-shcopykeyw.md) | Recursively copies the subkeys and values of the source subkey to the destination key. SHCopyKey does not copy the security attributes of the keys. |
| [SHCreateDataObject function](..\shlobj_core\nf-shlobj_core-shcreatedataobject.md) | Creates a data object in a parent folder. |
| [SHCreateDefaultContextMenu function](..\shlobj_core\nf-shlobj_core-shcreatedefaultcontextmenu.md) | Creates an object that represents the Shell's default context menu implementation. |
| [SHCreateDirectory function](..\shlobj_core\nf-shlobj_core-shcreatedirectory.md) | Creates a new file system folder. |
| [SHCreateDirectoryExA function](..\shlobj_core\nf-shlobj_core-shcreatedirectoryexa.md) | Creates a new file system folder, with optional security attributes. |
| [SHCreateDirectoryExW function](..\shlobj_core\nf-shlobj_core-shcreatedirectoryexw.md) | Creates a new file system folder, with optional security attributes. |
| [SHCreateFileExtractIconW function](..\shlobj_core\nf-shlobj_core-shcreatefileextracticonw.md) | SHCreateFileExtractIcon may be altered or unavailable. |
| [SHCreateMemStream function](..\shlwapi\nf-shlwapi-shcreatememstream.md) | Creates a memory stream using a similar process to CreateStreamOnHGlobal. |
| [SHCreateShellFolderView function](..\shlobj_core\nf-shlobj_core-shcreateshellfolderview.md) | Creates a new instance of the default Shell folder view object (DefView). |
| [SHCreateShellFolderViewEx function](..\shlobj_core\nf-shlobj_core-shcreateshellfolderviewex.md) | Creates a new instance of the default Shell folder view object. It is recommended that you use SHCreateShellFolderView rather than this function. |
| [SHCreateShellItem function](..\shlobj_core\nf-shlobj_core-shcreateshellitem.md) | Creates an IShellItem object. |
| [SHCreateShellPalette function](..\shlwapi\nf-shlwapi-shcreateshellpalette.md) | Creates a halftone palette for the specified device context. |
| [SHCreateStdEnumFmtEtc function](..\shlobj_core\nf-shlobj_core-shcreatestdenumfmtetc.md) | SHCreateStdEnumFmtEtc may be altered or unavailable. |
| [SHCreateStreamOnFileA function](..\shlwapi\nf-shlwapi-shcreatestreamonfilea.md) | SHCreateStreamOnFile may be altered or unavailable. Instead, use SHCreateStreamOnFileEx. |
| [SHCreateStreamOnFileEx function](..\shlwapi\nf-shlwapi-shcreatestreamonfileex.md) | Opens or creates a file and retrieves a stream to read or write to that file. |
| [SHCreateStreamOnFileW function](..\shlwapi\nf-shlwapi-shcreatestreamonfilew.md) | SHCreateStreamOnFile may be altered or unavailable. Instead, use SHCreateStreamOnFileEx. |
| [SHCreateThread function](..\shlwapi\nf-shlwapi-shcreatethread.md) | Creates a thread. |
| [SHCreateThreadRef function](..\shlwapi\nf-shlwapi-shcreatethreadref.md) | Creates a per-thread reference to a Component Object Model (COM) object. |
| [SHCreateThreadWithHandle function](..\shlwapi\nf-shlwapi-shcreatethreadwithhandle.md) | Creates a new thread and retrieves its handle. |
| [SHDefExtractIconA function](..\shlobj_core\nf-shlobj_core-shdefextracticona.md) | Provides a default handler to extract an icon from a file. |
| [SHDefExtractIconW function](..\shlobj_core\nf-shlobj_core-shdefextracticonw.md) | Provides a default handler to extract an icon from a file. |
| [SHDeleteEmptyKeyA function](..\shlwapi\nf-shlwapi-shdeleteemptykeya.md) | Deletes an empty key. |
| [SHDeleteEmptyKeyW function](..\shlwapi\nf-shlwapi-shdeleteemptykeyw.md) | Deletes an empty key. |
| [SHDeleteKeyA function](..\shlwapi\nf-shlwapi-shdeletekeya.md) | Deletes a subkey and all its descendants. This function removes the key and all the key's values from the registry. |
| [SHDeleteKeyW function](..\shlwapi\nf-shlwapi-shdeletekeyw.md) | Deletes a subkey and all its descendants. This function removes the key and all the key's values from the registry. |
| [SHDeleteValueA function](..\shlwapi\nf-shlwapi-shdeletevaluea.md) | Deletes a named value from the specified registry key. |
| [SHDeleteValueW function](..\shlwapi\nf-shlwapi-shdeletevaluew.md) | Deletes a named value from the specified registry key. |
| [SHDestroyPropSheetExtArray function](..\shlobj_core\nf-shlobj_core-shdestroypropsheetextarray.md) | Frees property sheet handlers that are pointed to an array created by SHCreatePropSheetExtArray. |
| [SHDoDragDrop function](..\shlobj_core\nf-shlobj_core-shdodragdrop.md) | Executes a drag-and-drop operation. Supports drag source creation on demand, as well as drag images. |
| [SHEnumKeyExA function](..\shlwapi\nf-shlwapi-shenumkeyexa.md) | Enumerates the subkeys of the specified open registry key. |
| [SHEnumKeyExW function](..\shlwapi\nf-shlwapi-shenumkeyexw.md) | Enumerates the subkeys of the specified open registry key. |
| [SHEnumValueA function](..\shlwapi\nf-shlwapi-shenumvaluea.md) | Enumerates the values of the specified open registry key. |
| [SHEnumValueW function](..\shlwapi\nf-shlwapi-shenumvaluew.md) | Enumerates the values of the specified open registry key. |
| [SHFindFiles function](..\shlobj_core\nf-shlobj_core-shfindfiles.md) | SHFindFiles may be altered or unavailable. |
| [SHFind_InitMenuPopup function](..\shlobj_core\nf-shlobj_core-shfind_initmenupopup.md) | SHFind_InitMenuPopup may be altered or unavailable. |
| [SHFlushSFCache function](..\shlobj_core\nf-shlobj_core-shflushsfcache.md) | SHFlushSFCache may be altered or unavailable. |
| [SHFormatDateTimeA function](..\shlwapi\nf-shlwapi-shformatdatetimea.md) | SHFormatDateTime may be altered or unavailable. |
| [SHFormatDateTimeW function](..\shlwapi\nf-shlwapi-shformatdatetimew.md) | SHFormatDateTime may be altered or unavailable. |
| [SHFormatDrive function](..\shlobj_core\nf-shlobj_core-shformatdrive.md) | SHFormatDrive may be altered or unavailable. |
| [SHFree function](..\shlobj_core\nf-shlobj_core-shfree.md) | Frees the memory allocated by SHAlloc. |
| [SHFreeShared function](..\shlwapi\nf-shlwapi-shfreeshared.md) | SHFreeShared may be altered or unavailable. |
| [SHGetAssocKeys function](..\shlwapi\nf-shlwapi-shgetassockeys.md) | Retrieves an array of class subkeys associated with an IQueryAssociations object. |
| [SHGetAttributesFromDataObject function](..\shlobj_core\nf-shlobj_core-shgetattributesfromdataobject.md) | SHGetAttributesFromDataObject may be altered or unavailable. |
| [SHGetDataFromIDListA function](..\shlobj_core\nf-shlobj_core-shgetdatafromidlista.md) | Retrieves extended property data from a relative identifier list. |
| [SHGetDataFromIDListW function](..\shlobj_core\nf-shlobj_core-shgetdatafromidlistw.md) | Retrieves extended property data from a relative identifier list. |
| [SHGetDesktopFolder function](..\shlobj_core\nf-shlobj_core-shgetdesktopfolder.md) | Retrieves the IShellFolder interface for the desktop folder, which is the root of the Shell's namespace. |
| [SHGetFolderLocation function](..\shlobj_core\nf-shlobj_core-shgetfolderlocation.md) | Deprecated. Retrieves the path of a folder as an ITEMIDLIST structure. |
| [SHGetFolderPathA function](..\shlobj_core\nf-shlobj_core-shgetfolderpatha.md) | Deprecated. |
| [SHGetFolderPathAndSubDirA function](..\shlobj_core\nf-shlobj_core-shgetfolderpathandsubdira.md) | Gets the path of a folder and appends a user-provided subfolder path. |
| [SHGetFolderPathAndSubDirW function](..\shlobj_core\nf-shlobj_core-shgetfolderpathandsubdirw.md) | Gets the path of a folder and appends a user-provided subfolder path. |
| [SHGetFolderPathW function](..\shlobj_core\nf-shlobj_core-shgetfolderpathw.md) | Deprecated. |
| [SHGetIconOverlayIndexA function](..\shlobj_core\nf-shlobj_core-shgeticonoverlayindexa.md) | Returns the index of the overlay icon in the system image list. |
| [SHGetIconOverlayIndexW function](..\shlobj_core\nf-shlobj_core-shgeticonoverlayindexw.md) | Returns the index of the overlay icon in the system image list. |
| [SHGetInstanceExplorer function](..\shlobj_core\nf-shlobj_core-shgetinstanceexplorer.md) | Retrieves an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. |
| [SHGetInverseCMAP function](..\shlwapi\nf-shlwapi-shgetinversecmap.md) | Retrieves the inverse color table mapping for the halftone palette. |
| [SHGetKnownFolderIDList function](..\shlobj_core\nf-shlobj_core-shgetknownfolderidlist.md) | Retrieves the path of a known folder as an ITEMIDLIST structure. |
| [SHGetKnownFolderItem function](..\shlobj_core\nf-shlobj_core-shgetknownfolderitem.md) | Retrieves an IShellItem object that represents a known folder. |
| [SHGetKnownFolderPath function](..\shlobj_core\nf-shlobj_core-shgetknownfolderpath.md) | Retrieves the full path of a known folder identified by the folder's KNOWNFOLDERID. |
| [SHGetMalloc function](..\shlobj_core\nf-shlobj_core-shgetmalloc.md) | Retrieves a pointer to the Shell's IMalloc interface. |
| [SHGetPathFromIDListA function](..\shlobj_core\nf-shlobj_core-shgetpathfromidlista.md) | Converts an item identifier list to a file system path. |
| [SHGetPathFromIDListEx function](..\shlobj_core\nf-shlobj_core-shgetpathfromidlistex.md) | Converts an item identifier list to a file system path. This function extends SHGetPathFromIDList by allowing you to set the initial size of the string buffer and declare the options below. |
| [SHGetPathFromIDListW function](..\shlobj_core\nf-shlobj_core-shgetpathfromidlistw.md) | Converts an item identifier list to a file system path. |
| [SHGetRealIDL function](..\shlobj_core\nf-shlobj_core-shgetrealidl.md) | SHGetRealIDL may be altered or unavailable. |
| [SHGetSetFolderCustomSettings function](..\shlobj_core\nf-shlobj_core-shgetsetfoldercustomsettings.md) | SHGetSetFolderCustomSettings may be altered or unavailable. |
| [SHGetSetSettings function](..\shlobj_core\nf-shlobj_core-shgetsetsettings.md) | SHGetSetSettings may be altered or unavailable. |
| [SHGetSettings function](..\shlobj_core\nf-shlobj_core-shgetsettings.md) | Retrieves the current Shell option settings. |
| [SHGetSpecialFolderLocation function](..\shlobj_core\nf-shlobj_core-shgetspecialfolderlocation.md) | SHGetSpecialFolderLocation is not supported and may be altered or unavailable in the future. Instead, use SHGetFolderLocation. |
| [SHGetSpecialFolderPathA function](..\shlobj_core\nf-shlobj_core-shgetspecialfolderpatha.md) | SHGetSpecialFolderPath is not supported. Instead, use ShGetFolderPath. |
| [SHGetSpecialFolderPathW function](..\shlobj_core\nf-shlobj_core-shgetspecialfolderpathw.md) | SHGetSpecialFolderPath is not supported. Instead, use ShGetFolderPath. |
| [SHGetThreadRef function](..\shlwapi\nf-shlwapi-shgetthreadref.md) | Retrieves the per-thread object reference set by SHSetThreadRef. |
| [SHGetValueA function](..\shlwapi\nf-shlwapi-shgetvaluea.md) | Retrieves a registry value. |
| [SHGetValueW function](..\shlwapi\nf-shlwapi-shgetvaluew.md) | Retrieves a registry value. |
| [SHGetViewStatePropertyBag function](..\shlwapi\nf-shlwapi-shgetviewstatepropertybag.md) | SHGetViewStatePropertyBag may be altered or unavailable. |
| [SHGlobalCounterDecrement function](..\shlwapi\nf-shlwapi-shglobalcounterdecrement.md) | Decrements a global counter. |
| [SHGlobalCounterGetValue function](..\shlwapi\nf-shlwapi-shglobalcountergetvalue.md) | Gets the current value of a global counter. |
| [SHGlobalCounterIncrement function](..\shlwapi\nf-shlwapi-shglobalcounterincrement.md) | Increments a global counter. |
| [SHHandleUpdateImage function](..\shlobj_core\nf-shlobj_core-shhandleupdateimage.md) | SHHandleUpdateImage may be altered or unavailable. |
| [SHILCreateFromPath function](..\shlobj_core\nf-shlobj_core-shilcreatefrompath.md) | SHILCreateFromPath may be altered or unavailable. |
| [SHLimitInputEdit function](..\shlobj_core\nf-shlobj_core-shlimitinputedit.md) | Sets limits on valid characters for an edit control. |
| [SHLoadInProc function](..\shlobj_core\nf-shlobj_core-shloadinproc.md) | Creates an instance of the specified object class from within the context of the Shell's process. Windows Vista and later |
| [SHLoadIndirectString function](..\shlwapi\nf-shlwapi-shloadindirectstring.md) | Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol). |
| [SHLocalStrDupA function](..\shlwapi\nf-shlwapi-shlocalstrdupa.md) | Makes a copy of a string in newly allocated memory. |
| [SHLocalStrDupW function](..\shlwapi\nf-shlwapi-shlocalstrdupw.md) | Makes a copy of a string in newly allocated memory. |
| [SHLockShared function](..\shlwapi\nf-shlwapi-shlockshared.md) | SHLockShared may be altered or unavailable. |
| [SHMapPIDLToSystemImageListIndex function](..\shlobj_core\nf-shlobj_core-shmappidltosystemimagelistindex.md) | SHMapPIDLToSystemImageListIndex may be altered or unavailable. |
| [SHMessageBoxCheckA function](..\shlwapi\nf-shlwapi-shmessageboxchecka.md) | SHMessageBoxCheck may be altered or unavailable. |
| [SHMessageBoxCheckW function](..\shlwapi\nf-shlwapi-shmessageboxcheckw.md) | SHMessageBoxCheck may be altered or unavailable. |
| [SHObjectProperties function](..\shlobj_core\nf-shlobj_core-shobjectproperties.md) | SHObjectProperties may be altered or unavailable. |
| [SHOpenFolderAndSelectItems function](..\shlobj_core\nf-shlobj_core-shopenfolderandselectitems.md) | Opens a Windows Explorer window with specified items in a particular folder selected. |
| [SHOpenRegStream2A function](..\shlwapi\nf-shlwapi-shopenregstream2a.md) | Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes SHOpenRegStream. |
| [SHOpenRegStream2W function](..\shlwapi\nf-shlwapi-shopenregstream2w.md) | Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes SHOpenRegStream. |
| [SHOpenRegStreamA function](..\shlwapi\nf-shlwapi-shopenregstreama.md) | Deprecated. |
| [SHOpenRegStreamW function](..\shlwapi\nf-shlwapi-shopenregstreamw.md) | Deprecated. |
| [SHOpenWithDialog function](..\shlobj_core\nf-shlobj_core-shopenwithdialog.md) | Displays the Open With dialog box. |
| [SHParseDisplayName function](..\shlobj_core\nf-shlobj_core-shparsedisplayname.md) | Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object. This function is the preferred method to convert a string to a pointer to an item identifier list (PIDL). |
| [SHPathPrepareForWriteA function](..\shlobj_core\nf-shlobj_core-shpathprepareforwritea.md) | Checks to see if the path exists. |
| [SHPathPrepareForWriteW function](..\shlobj_core\nf-shlobj_core-shpathprepareforwritew.md) | Checks to see if the path exists. |
| [SHQueryInfoKeyA function](..\shlwapi\nf-shlwapi-shqueryinfokeya.md) | Retrieves information about a specified registry key. |
| [SHQueryInfoKeyW function](..\shlwapi\nf-shlwapi-shqueryinfokeyw.md) | Retrieves information about a specified registry key. |
| [SHQueryValueExA function](..\shlwapi\nf-shlwapi-shqueryvalueexa.md) | Opens a registry key and queries it for a specific value. |
| [SHQueryValueExW function](..\shlwapi\nf-shlwapi-shqueryvalueexw.md) | Opens a registry key and queries it for a specific value. |
| [SHRegCloseUSKey function](..\shlwapi\nf-shlwapi-shregcloseuskey.md) | Closes a handle to a user-specific registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegCreateUSKeyA function](..\shlwapi\nf-shlwapi-shregcreateuskeya.md) | Creates or opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegCreateUSKeyW function](..\shlwapi\nf-shlwapi-shregcreateuskeyw.md) | Creates or opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegDeleteEmptyUSKeyA function](..\shlwapi\nf-shlwapi-shregdeleteemptyuskeya.md) | Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegDeleteEmptyUSKeyW function](..\shlwapi\nf-shlwapi-shregdeleteemptyuskeyw.md) | Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegDeleteUSValueA function](..\shlwapi\nf-shlwapi-shregdeleteusvaluea.md) | Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegDeleteUSValueW function](..\shlwapi\nf-shlwapi-shregdeleteusvaluew.md) | Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegDuplicateHKey function](..\shlwapi\nf-shlwapi-shregduplicatehkey.md) | Duplicates a registry key's HKEY handle. |
| [SHRegEnumUSKeyA function](..\shlwapi\nf-shlwapi-shregenumuskeya.md) | Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegEnumUSKeyW function](..\shlwapi\nf-shlwapi-shregenumuskeyw.md) | Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegEnumUSValueA function](..\shlwapi\nf-shlwapi-shregenumusvaluea.md) | Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegEnumUSValueW function](..\shlwapi\nf-shlwapi-shregenumusvaluew.md) | Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegGetBoolUSValueA function](..\shlwapi\nf-shlwapi-shreggetboolusvaluea.md) | Retrieves a Boolean value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegGetBoolUSValueW function](..\shlwapi\nf-shlwapi-shreggetboolusvaluew.md) | Retrieves a Boolean value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegGetBoolValueFromHKCUHKLM function](..\shlwapi\nf-shlwapi-shreggetboolvaluefromhkcuhklm.md) | Evaluates a registry key value and returns a boolean value that reflects whether the value exists and the expected state matches the actual state. |
| [SHRegGetIntW function](..\shlwapi\nf-shlwapi-shreggetintw.md) | Reads a numeric string value from the registry and converts it to an integer. |
| [SHRegGetPathA function](..\shlwapi\nf-shlwapi-shreggetpatha.md) | Retrieves a file path from the registry, expanding environment variables as needed. |
| [SHRegGetPathW function](..\shlwapi\nf-shlwapi-shreggetpathw.md) | Retrieves a file path from the registry, expanding environment variables as needed. |
| [SHRegGetUSValueA function](..\shlwapi\nf-shlwapi-shreggetusvaluea.md) | Retrieves a value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegGetUSValueW function](..\shlwapi\nf-shlwapi-shreggetusvaluew.md) | Retrieves a value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegGetValueA function](..\shlwapi\nf-shlwapi-shreggetvaluea.md) | Retrieves a registry value. |
| [SHRegGetValueFromHKCUHKLM function](..\shlwapi\nf-shlwapi-shreggetvaluefromhkcuhklm.md) | Obtains specified information from the registry. |
| [SHRegGetValueW function](..\shlwapi\nf-shlwapi-shreggetvaluew.md) | Retrieves a registry value. |
| [SHRegOpenUSKeyA function](..\shlwapi\nf-shlwapi-shregopenuskeya.md) | Opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegOpenUSKeyW function](..\shlwapi\nf-shlwapi-shregopenuskeyw.md) | Opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegQueryInfoUSKeyA function](..\shlwapi\nf-shlwapi-shregqueryinfouskeya.md) | Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegQueryInfoUSKeyW function](..\shlwapi\nf-shlwapi-shregqueryinfouskeyw.md) | Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegQueryUSValueA function](..\shlwapi\nf-shlwapi-shregqueryusvaluea.md) | Retrieves the type and data for a specified name associated with an open registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegQueryUSValueW function](..\shlwapi\nf-shlwapi-shregqueryusvaluew.md) | Retrieves the type and data for a specified name associated with an open registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegSetPathA function](..\shlwapi\nf-shlwapi-shregsetpatha.md) | Takes a file path, replaces folder names with environment strings, and places the resulting string in the registry. |
| [SHRegSetPathW function](..\shlwapi\nf-shlwapi-shregsetpathw.md) | Takes a file path, replaces folder names with environment strings, and places the resulting string in the registry. |
| [SHRegSetUSValueA function](..\shlwapi\nf-shlwapi-shregsetusvaluea.md) | Sets a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegSetUSValueW function](..\shlwapi\nf-shlwapi-shregsetusvaluew.md) | Sets a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegWriteUSValueA function](..\shlwapi\nf-shlwapi-shregwriteusvaluea.md) | Writes a value to a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHRegWriteUSValueW function](..\shlwapi\nf-shlwapi-shregwriteusvaluew.md) | Writes a value to a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). |
| [SHReleaseThreadRef function](..\shlwapi\nf-shlwapi-shreleasethreadref.md) | Releases a thread reference before the thread procedure returns. |
| [SHReplaceFromPropSheetExtArray function](..\shlobj_core\nf-shlobj_core-shreplacefrompropsheetextarray.md) | Requests each property sheet in a property sheet extension array to replace pages. Each page is allowed up to one replacement. |
| [SHRestricted function](..\shlobj_core\nf-shlobj_core-shrestricted.md) | SHRestricted may be altered or unavailable. |
| [SHSendMessageBroadcastA function](..\shlwapi\nf-shlwapi-shsendmessagebroadcasta.md) | Sends a message to all top-level windows in the system. |
| [SHSendMessageBroadcastW function](..\shlwapi\nf-shlwapi-shsendmessagebroadcastw.md) | Sends a message to all top-level windows in the system. |
| [SHSetFolderPathA function](..\shlobj_core\nf-shlobj_core-shsetfolderpatha.md) | Deprecated. Assigns a new path to a system folder identified by its CSIDL. |
| [SHSetFolderPathW function](..\shlobj_core\nf-shlobj_core-shsetfolderpathw.md) | Deprecated. Assigns a new path to a system folder identified by its CSIDL. |
| [SHSetInstanceExplorer function](..\shlobj_core\nf-shlobj_core-shsetinstanceexplorer.md) | Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. |
| [SHSetKnownFolderPath function](..\shlobj_core\nf-shlobj_core-shsetknownfolderpath.md) | Redirects a known folder to a new location. |
| [SHSetThreadRef function](..\shlwapi\nf-shlwapi-shsetthreadref.md) | Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready. |
| [SHSetValueA function](..\shlwapi\nf-shlwapi-shsetvaluea.md) | Sets the value of a registry key. |
| [SHSetValueW function](..\shlwapi\nf-shlwapi-shsetvaluew.md) | Sets the value of a registry key. |
| [SHShellFolderView_Message function](..\shlobj_core\nf-shlobj_core-shshellfolderview_message.md) | SHShellFolderView_Message may be altered or unavailable. |
| [SHSkipJunction function](..\shlwapi\nf-shlwapi-shskipjunction.md) | Checks a bind context to see if it is safe to bind to a particular component object. |
| [SHStartNetConnectionDialogA function](..\shlobj_core\nf-shlobj_core-shstartnetconnectiondialoga.md) | SHStartNetConnectionDialog may be altered or unavailable. |
| [SHStartNetConnectionDialogW function](..\shlobj_core\nf-shlobj_core-shstartnetconnectiondialogw.md) | SHStartNetConnectionDialog may be altered or unavailable. |
| [SHStrDupA function](..\shlwapi\nf-shlwapi-shstrdupa.md) | Makes a copy of a string in newly allocated memory. |
| [SHStrDupW function](..\shlwapi\nf-shlwapi-shstrdupw.md) | Makes a copy of a string in newly allocated memory. |
| [SHStripMneumonicA function](..\shlwapi\nf-shlwapi-shstripmneumonica.md) | Removes the mnemonic marker from a string. |
| [SHStripMneumonicW function](..\shlwapi\nf-shlwapi-shstripmneumonicw.md) | Removes the mnemonic marker from a string. |
| [SHUnicodeToAnsi function](..\shlwapi\nf-shlwapi-shunicodetoansi.md) | Converts a string from the Unicode code page to the ANSI code page. |
| [SHUnicodeToUnicode function](..\shlwapi\nf-shlwapi-shunicodetounicode.md) | Copies a Unicode string. |
| [SHUnlockShared function](..\shlwapi\nf-shlwapi-shunlockshared.md) | SHUnlockShared may be altered or unavailable. |
| [SHUpdateImageA function](..\shlobj_core\nf-shlobj_core-shupdateimagea.md) | Notifies the Shell that an image in the system image list has changed. |
| [SHUpdateImageW function](..\shlobj_core\nf-shlobj_core-shupdateimagew.md) | Notifies the Shell that an image in the system image list has changed. |
| [SHValidateUNC function](..\shlobj_core\nf-shlobj_core-shvalidateunc.md) | SHValidateUNC may be altered or unavailable. |
| [SSIZETAdd function](..\intsafe\nf-intsafe-ssizetadd.md) | Adds two SSIZE_T values together. |
| [SSIZETMult function](..\intsafe\nf-intsafe-ssizetmult.md) | Multiplies one SSIZE_T value by another. |
| [SSIZETSub function](..\intsafe\nf-intsafe-ssizetsub.md) | Subtracts one SSIZE_T value from another. |
| [ScreenSaverConfigureDialog function](..\scrnsave\nf-scrnsave-screensaverconfiguredialog.md) | Receives messages sent to a screen saver's configuration dialog box. A screen saver that allows user configuration must define this function. |
| [ScreenSaverProc function](..\scrnsave\nf-scrnsave-screensaverproc.md) | Receives messages sent to the specified screen saver window. |
| [SetProcessReference function](..\shlwapi\nf-shlwapi-setprocessreference.md) | Provides a Component Object Model (COM) object that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. |
| [Shell_GetCachedImageIndex function](..\shlobj_core\nf-shlobj_core-shell_getcachedimageindex.md) | Shell_GetCachedImageIndex may be altered or unavailable. |
| [Shell_GetCachedImageIndexA function](..\shlobj_core\nf-shlobj_core-shell_getcachedimageindexa.md) | Shell_GetCachedImageIndex may be altered or unavailable. |
| [Shell_GetCachedImageIndexW function](..\shlobj_core\nf-shlobj_core-shell_getcachedimageindexw.md) | Shell_GetCachedImageIndex may be altered or unavailable. |
| [Shell_GetImageLists function](..\shlobj_core\nf-shlobj_core-shell_getimagelists.md) | Retrieves system image lists for large and small icons. |
| [Shell_MergeMenus function](..\shlobj_core\nf-shlobj_core-shell_mergemenus.md) | Shell_MergeMenus may be altered or unavailable. |
| [ShortAdd function](..\intsafe\nf-intsafe-shortadd.md) | Adds two values of type SHORT. |
| [ShortMult function](..\intsafe\nf-intsafe-shortmult.md) | Multiplies two values of type SHORT. |
| [ShortSub function](..\intsafe\nf-intsafe-shortsub.md) | Subtracts one value of type SHORT from another. |
| [ShortToChar function](..\intsafe\nf-intsafe-shorttochar.md) | Converts a value of type SHORT to a value of CHAR. |
| [ShortToDWordPtr function](..\intsafe\nf-intsafe-shorttodwordptr.md) | Converts a value of type SHORT to a value of type DWORD_PTR. |
| [ShortToInt8 function](..\intsafe\nf-intsafe-shorttoint8.md) | Converts a value of type SHORT to a value of type INT8. |
| [ShortToUChar function](..\intsafe\nf-intsafe-shorttouchar.md) | Converts a value of type SHORT to a value of UCHAR. |
| [ShortToUInt function](..\intsafe\nf-intsafe-shorttouint.md) | Converts a value of type SHORT to a value of type UINT. |
| [ShortToUInt8 function](..\intsafe\nf-intsafe-shorttouint8.md) | Converts a value of type SHORT to a value of type BYTE. |
| [ShortToUIntPtr function](..\intsafe\nf-intsafe-shorttouintptr.md) | Converts a value of type SHORT to a value of type UINT_PTR. |
| [ShortToULong function](..\intsafe\nf-intsafe-shorttoulong.md) | Converts a value of type SHORT to a value of type ULONG. |
| [ShortToULongLong function](..\intsafe\nf-intsafe-shorttoulonglong.md) | Converts a value of type SHORT to a value of type ULONGLONG. |
| [ShortToULongPtr function](..\intsafe\nf-intsafe-shorttoulongptr.md) | Converts a value of type SHORT to a value of type ULONG_PTR. |
| [ShortToUShort function](..\intsafe\nf-intsafe-shorttoushort.md) | Converts a value of type SHORT to a value of type USHORT. |
| [SignalFileOpen function](..\shlobj_core\nf-shlobj_core-signalfileopen.md) | SignalFileOpen may be altered or unavailable. |
| [SizeTAdd function](..\intsafe\nf-intsafe-sizetadd.md) | Adds two values of type size_t. |
| [SizeTMult function](..\intsafe\nf-intsafe-sizetmult.md) | Multiplies one value of type size_t by another. |
| [SizeTSub function](..\intsafe\nf-intsafe-sizetsub.md) | Subtracts one value of type size_t from another. |
| [StgMakeUniqueName function](..\shlobj_core\nf-shlobj_core-stgmakeuniquename.md) | Creates a unique name for a stream or storage object from a template. |
| [StopWatchFlush function](..\shlwapi\nf-shlwapi-stopwatchflush.md) | StopWatchFlush may be altered or unavailable. |
| [StopWatchMode function](..\shlwapi\nf-shlwapi-stopwatchmode.md) | StopWatchMode may be altered or unavailable. |
| [StrCSpnA function](..\shlwapi\nf-shlwapi-strcspna.md) | Searches a string for the first occurrence of any of a group of characters. The search method is case-sensitive, and the terminating NULL character is included within the search pattern match. |
| [StrCSpnIA function](..\shlwapi\nf-shlwapi-strcspnia.md) | Searches a string for the first occurrence of any of a group of characters. The search method is not case-sensitive, and the terminating NULL character is included within the search pattern match. |
| [StrCSpnIW function](..\shlwapi\nf-shlwapi-strcspniw.md) | Searches a string for the first occurrence of any of a group of characters. The search method is not case-sensitive, and the terminating NULL character is included within the search pattern match. |
| [StrCSpnW function](..\shlwapi\nf-shlwapi-strcspnw.md) | Searches a string for the first occurrence of any of a group of characters. The search method is case-sensitive, and the terminating NULL character is included within the search pattern match. |
| [StrCatBuffA function](..\shlwapi\nf-shlwapi-strcatbuffa.md) | Copies and appends characters from one string to the end of another. |
| [StrCatBuffW function](..\shlwapi\nf-shlwapi-strcatbuffw.md) | Copies and appends characters from one string to the end of another. |
| [StrCatChainW function](..\shlwapi\nf-shlwapi-strcatchainw.md) | Concatenates two Unicode strings. Used when repeated concatenations to the same buffer are required. |
| [StrCatW function](..\shlwapi\nf-shlwapi-strcatw.md) | Appends one string to another. |
| [StrChrA function](..\shlwapi\nf-shlwapi-strchra.md) | Searches a string for the first occurrence of a character that matches the specified character. The comparison is case-sensitive. |
| [StrChrIA function](..\shlwapi\nf-shlwapi-strchria.md) | Searches a string for the first occurrence of a character that matches the specified character. The comparison is not case-sensitive. |
| [StrChrIW function](..\shlwapi\nf-shlwapi-strchriw.md) | Searches a string for the first occurrence of a character that matches the specified character. The comparison is not case-sensitive. |
| [StrChrNIW function](..\shlwapi\nf-shlwapi-strchrniw.md) | Searches a string for the first occurrence of a specified character. The comparison is not case-sensitive. |
| [StrChrNW function](..\shlwapi\nf-shlwapi-strchrnw.md) | Searches a string for the first occurrence of a specified character. The comparison is case-sensitive. |
| [StrChrW function](..\shlwapi\nf-shlwapi-strchrw.md) | Searches a string for the first occurrence of a character that matches the specified character. The comparison is case-sensitive. |
| [StrCmpCA function](..\shlwapi\nf-shlwapi-strcmpca.md) | Compares strings using C run-time (ASCII) collation rules. The comparison is case-sensitive. |
| [StrCmpCW function](..\shlwapi\nf-shlwapi-strcmpcw.md) | Compares strings using C run-time (ASCII) collation rules. The comparison is case-sensitive. |
| [StrCmpICA function](..\shlwapi\nf-shlwapi-strcmpica.md) | Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. |
| [StrCmpICW function](..\shlwapi\nf-shlwapi-strcmpicw.md) | Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. |
| [StrCmpIW function](..\shlwapi\nf-shlwapi-strcmpiw.md) | Compares two strings to determine if they are the same. The comparison is not case-sensitive. |
| [StrCmpLogicalW function](..\shlwapi\nf-shlwapi-strcmplogicalw.md) | Compares two Unicode strings. Digits in the strings are considered as numerical content rather than text. This test is not case-sensitive. |
| [StrCmpNA function](..\shlwapi\nf-shlwapi-strcmpna.md) | Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is case-sensitive. The StrNCmp macro differs from this function in name only. |
| [StrCmpNCA function](..\shlwapi\nf-shlwapi-strcmpnca.md) | Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is case-sensitive. |
| [StrCmpNCW function](..\shlwapi\nf-shlwapi-strcmpncw.md) | Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is case-sensitive. |
| [StrCmpNIA function](..\shlwapi\nf-shlwapi-strcmpnia.md) | Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is not case-sensitive. The StrNCmpI macro differs from this function in name only. |
| [StrCmpNICA function](..\shlwapi\nf-shlwapi-strcmpnica.md) | Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. |
| [StrCmpNICW function](..\shlwapi\nf-shlwapi-strcmpnicw.md) | Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. |
| [StrCmpNIW function](..\shlwapi\nf-shlwapi-strcmpniw.md) | Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is not case-sensitive. The StrNCmpI macro differs from this function in name only. |
| [StrCmpNW function](..\shlwapi\nf-shlwapi-strcmpnw.md) | Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is case-sensitive. The StrNCmp macro differs from this function in name only. |
| [StrCmpW function](..\shlwapi\nf-shlwapi-strcmpw.md) | Compares two strings to determine if they are the same. The comparison is case-sensitive. |
| [StrCpyNW function](..\shlwapi\nf-shlwapi-strcpynw.md) | Copies a specified number of characters from the beginning of one string to another.Note  Do not use this function or the StrNCpy macro. |
| [StrCpyW function](..\shlwapi\nf-shlwapi-strcpyw.md) | Copies one string to another. |
| [StrDupA function](..\shlwapi\nf-shlwapi-strdupa.md) | Duplicates a string. |
| [StrDupW function](..\shlwapi\nf-shlwapi-strdupw.md) | Duplicates a string. |
| [StrFormatByteSize64A function](..\shlwapi\nf-shlwapi-strformatbytesize64a.md) | Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size. |
| [StrFormatByteSizeA function](..\shlwapi\nf-shlwapi-strformatbytesizea.md) | Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size. Differs from StrFormatByteSizeW in one parameter type. |
| [StrFormatByteSizeEx function](..\shlwapi\nf-shlwapi-strformatbytesizeex.md) | Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size. |
| [StrFormatByteSizeW function](..\shlwapi\nf-shlwapi-strformatbytesizew.md) | Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size. Differs from StrFormatByteSizeA in one parameter type. |
| [StrFormatKBSizeA function](..\shlwapi\nf-shlwapi-strformatkbsizea.md) | Converts a numeric value into a string that represents the number expressed as a size value in kilobytes. |
| [StrFormatKBSizeW function](..\shlwapi\nf-shlwapi-strformatkbsizew.md) | Converts a numeric value into a string that represents the number expressed as a size value in kilobytes. |
| [StrFromTimeIntervalA function](..\shlwapi\nf-shlwapi-strfromtimeintervala.md) | Converts a time interval, specified in milliseconds, to a string. |
| [StrFromTimeIntervalW function](..\shlwapi\nf-shlwapi-strfromtimeintervalw.md) | Converts a time interval, specified in milliseconds, to a string. |
| [StrIsIntlEqualA function](..\shlwapi\nf-shlwapi-strisintlequala.md) | Compares a specified number of characters from the beginning of two strings to determine if they are equal. |
| [StrIsIntlEqualW function](..\shlwapi\nf-shlwapi-strisintlequalw.md) | Compares a specified number of characters from the beginning of two strings to determine if they are equal. |
| [StrNCatA function](..\shlwapi\nf-shlwapi-strncata.md) | Appends a specified number of characters from the beginning of one string to the end of another. |
| [StrNCatW function](..\shlwapi\nf-shlwapi-strncatw.md) | Appends a specified number of characters from the beginning of one string to the end of another. |
| [StrPBrkA function](..\shlwapi\nf-shlwapi-strpbrka.md) | Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character. |
| [StrPBrkW function](..\shlwapi\nf-shlwapi-strpbrkw.md) | Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character. |
| [StrRChrA function](..\shlwapi\nf-shlwapi-strrchra.md) | Searches a string for the last occurrence of a specified character. The comparison is case-sensitive. |
| [StrRChrIA function](..\shlwapi\nf-shlwapi-strrchria.md) | Searches a string for the last occurrence of a specified character. The comparison is not case-sensitive. |
| [StrRChrIW function](..\shlwapi\nf-shlwapi-strrchriw.md) | Searches a string for the last occurrence of a specified character. The comparison is not case-sensitive. |
| [StrRChrW function](..\shlwapi\nf-shlwapi-strrchrw.md) | Searches a string for the last occurrence of a specified character. The comparison is case-sensitive. |
| [StrRStrIA function](..\shlwapi\nf-shlwapi-strrstria.md) | Searches for the last occurrence of a specified substring within a string. The comparison is not case-sensitive. |
| [StrRStrIW function](..\shlwapi\nf-shlwapi-strrstriw.md) | Searches for the last occurrence of a specified substring within a string. The comparison is not case-sensitive. |
| [StrRetToBSTR function](..\shlwapi\nf-shlwapi-strrettobstr.md) | Accepts a STRRET structure returned by IShellFolder |
| [StrRetToBufA function](..\shlwapi\nf-shlwapi-strrettobufa.md) | Converts an STRRET structure returned by IShellFolder |
| [StrRetToBufW function](..\shlwapi\nf-shlwapi-strrettobufw.md) | Converts an STRRET structure returned by IShellFolder |
| [StrRetToStrA function](..\shlwapi\nf-shlwapi-strrettostra.md) | Takes an STRRET structure returned by IShellFolder |
| [StrRetToStrW function](..\shlwapi\nf-shlwapi-strrettostrw.md) | Takes an STRRET structure returned by IShellFolder |
| [StrSpnA function](..\shlwapi\nf-shlwapi-strspna.md) | Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer. |
| [StrSpnW function](..\shlwapi\nf-shlwapi-strspnw.md) | Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer. |
| [StrStrA function](..\shlwapi\nf-shlwapi-strstra.md) | Finds the first occurrence of a substring within a string. The comparison is case-sensitive. |
| [StrStrIA function](..\shlwapi\nf-shlwapi-strstria.md) | Finds the first occurrence of a substring within a string. The comparison is not case-sensitive. |
| [StrStrIW function](..\shlwapi\nf-shlwapi-strstriw.md) | Finds the first occurrence of a substring within a string. The comparison is not case-sensitive. |
| [StrStrNIW function](..\shlwapi\nf-shlwapi-strstrniw.md) | Finds the first occurrence of a substring within a string. The comparison is case-insensitive. |
| [StrStrNW function](..\shlwapi\nf-shlwapi-strstrnw.md) | Finds the first occurrence of a substring within a string. The comparison is case-sensitive. |
| [StrStrW function](..\shlwapi\nf-shlwapi-strstrw.md) | Finds the first occurrence of a substring within a string. The comparison is case-sensitive. |
| [StrToInt64ExA function](..\shlwapi\nf-shlwapi-strtoint64exa.md) | Converts a string representing a decimal or hexadecimal value to a 64-bit integer. |
| [StrToInt64ExW function](..\shlwapi\nf-shlwapi-strtoint64exw.md) | Converts a string representing a decimal or hexadecimal value to a 64-bit integer. |
| [StrToIntA function](..\shlwapi\nf-shlwapi-strtointa.md) | Converts a string that represents a decimal value to an integer. The StrToLong macro is identical to this function. |
| [StrToIntExA function](..\shlwapi\nf-shlwapi-strtointexa.md) | Converts a string representing a decimal or hexadecimal number to an integer. |
| [StrToIntExW function](..\shlwapi\nf-shlwapi-strtointexw.md) | Converts a string representing a decimal or hexadecimal number to an integer. |
| [StrToIntW function](..\shlwapi\nf-shlwapi-strtointw.md) | Converts a string that represents a decimal value to an integer. The StrToLong macro is identical to this function. |
| [StrTrimA function](..\shlwapi\nf-shlwapi-strtrima.md) | Removes specified leading and trailing characters from a string. |
| [StrTrimW function](..\shlwapi\nf-shlwapi-strtrimw.md) | Removes specified leading and trailing characters from a string. |
| [TranslateURLA function](..\intshcut\nf-intshcut-translateurla.md) | Applies common translations to a given URL string, creating a new URL string. |
| [TranslateURLW function](..\intshcut\nf-intshcut-translateurlw.md) | Applies common translations to a given URL string, creating a new URL string. |
| [UInt8Add function](..\intsafe\nf-intsafe-uint8add.md) | Adds two values of type UINT8. |
| [UInt8Mult function](..\intsafe\nf-intsafe-uint8mult.md) | Multiplies two values of type UINT8. |
| [UInt8Sub function](..\intsafe\nf-intsafe-uint8sub.md) | Subtracts one value of type UINT8 from another. |
| [UInt8ToChar function](..\intsafe\nf-intsafe-uint8tochar.md) | Converts a value of type UINT8 to a value of type CHAR. |
| [UInt8ToInt8 function](..\intsafe\nf-intsafe-uint8toint8.md) | Converts a value of type UINT8 to a value of type INT8. |
| [UIntAdd function](..\intsafe\nf-intsafe-uintadd.md) | Adds two values of type UINT. |
| [UIntMult function](..\intsafe\nf-intsafe-uintmult.md) | Multiplies one value of type UINT by another. |
| [UIntPtrAdd function](..\intsafe\nf-intsafe-uintptradd.md) | Adds two values of type UINT_PTR. |
| [UIntPtrMult function](..\intsafe\nf-intsafe-uintptrmult.md) | Multiplies one value of type UINT_PTR by another. |
| [UIntPtrSub function](..\intsafe\nf-intsafe-uintptrsub.md) | Subtracts one value of type UINT_PTR from another. |
| [UIntPtrToChar function](..\intsafe\nf-intsafe-uintptrtochar.md) | Converts a value of type UINT_PTR to a value of type CHAR. |
| [UIntPtrToInt function](..\intsafe\nf-intsafe-uintptrtoint.md) | Converts a value of type SIZE_T to a value of type INT. |
| [UIntPtrToInt16 function](..\intsafe\nf-intsafe-uintptrtoint16.md) | Converts a value of type UINT_PTR to a value of type INT16. |
| [UIntPtrToInt8 function](..\intsafe\nf-intsafe-uintptrtoint8.md) | Converts a value of type UINT_PTR to a value of type INT8. |
| [UIntPtrToIntPtr function](..\intsafe\nf-intsafe-uintptrtointptr.md) | Converts a value of type size_t to a value of type INT_PTR. |
| [UIntPtrToLong function](..\intsafe\nf-intsafe-uintptrtolong.md) | Converts a value of type size_t to a value of type LONG. |
| [UIntPtrToLongLong function](..\intsafe\nf-intsafe-uintptrtolonglong.md) | Converts a value of type UINT_PTR to a value of type LONGLONG. |
| [UIntPtrToLongPtr function](..\intsafe\nf-intsafe-uintptrtolongptr.md) | Converts a value of type size_t to a value of type LONG_PTR. |
| [UIntPtrToShort function](..\intsafe\nf-intsafe-uintptrtoshort.md) | Converts a value of type UINT_PTR to a value of type SHORT. |
| [UIntPtrToUChar function](..\intsafe\nf-intsafe-uintptrtouchar.md) | Converts a value of type UINT_PTR to a value of type UCHAR. |
| [UIntPtrToUInt function](..\intsafe\nf-intsafe-uintptrtouint.md) | Converts a value of type size_t to a value of type UINT. |
| [UIntPtrToUInt16 function](..\intsafe\nf-intsafe-uintptrtouint16.md) | Converts a value of type UINT_PTR to a value of type UINT16. |
| [UIntPtrToUInt8 function](..\intsafe\nf-intsafe-uintptrtouint8.md) | Converts a value of type UINT_PTR to a value of type UINT8. |
| [UIntPtrToULong function](..\intsafe\nf-intsafe-uintptrtoulong.md) | Converts a value of type SIZE_T to a value of type DWORD. |
| [UIntPtrToUShort function](..\intsafe\nf-intsafe-uintptrtoushort.md) | Converts a value of type UINT_PTR to a value of type USHORT. |
| [UIntSub function](..\intsafe\nf-intsafe-uintsub.md) | Subtracts one value of type UINT from another. |
| [UIntToChar function](..\intsafe\nf-intsafe-uinttochar.md) | Converts a value of type UINT to a value of type CHAR. |
| [UIntToInt function](..\intsafe\nf-intsafe-uinttoint.md) | Converts a value of type UINT to a value of type INT. |
| [UIntToInt8 function](..\intsafe\nf-intsafe-uinttoint8.md) | Converts a value of type UINT to a value of type INT8. |
| [UIntToIntPtr function](..\intsafe\nf-intsafe-uinttointptr.md) | Converts a value of type UINT to a value of type INT_PTR. |
| [UIntToLong function](..\intsafe\nf-intsafe-uinttolong.md) | Converts a value of type UINT to a value of type LONG. |
| [UIntToLongPtr function](..\intsafe\nf-intsafe-uinttolongptr.md) | Converts a value of type UINT to a value of type LONG_PTR. |
| [UIntToShort function](..\intsafe\nf-intsafe-uinttoshort.md) | Converts a value of type UINT to a value of type SHORT. |
| [UIntToUChar function](..\intsafe\nf-intsafe-uinttouchar.md) | Converts a value of type UINT to a value of type UCHAR. |
| [UIntToUInt8 function](..\intsafe\nf-intsafe-uinttouint8.md) | Converts a value of type UINT to a value of type BYTE. |
| [UIntToUShort function](..\intsafe\nf-intsafe-uinttoushort.md) | Converts a value of type UINT to a value of type USHORT. |
| [ULongAdd function](..\intsafe\nf-intsafe-ulongadd.md) | Adds two values of type DWORD. |
| [ULongLongAdd function](..\intsafe\nf-intsafe-ulonglongadd.md) | Adds two values of type SIZE_T. |
| [ULongLongMult function](..\intsafe\nf-intsafe-ulonglongmult.md) | Multiplies one value of type size_t by another. |
| [ULongLongSub function](..\intsafe\nf-intsafe-ulonglongsub.md) | Subtracts one value of type SIZE_T from another. |
| [ULongLongToChar function](..\intsafe\nf-intsafe-ulonglongtochar.md) | Converts a value of type ULONGLONG to a value of type CHAR. |
| [ULongLongToInt function](..\intsafe\nf-intsafe-ulonglongtoint.md) | Converts a value of type ULONGLONG to a value of type INT. |
| [ULongLongToInt8 function](..\intsafe\nf-intsafe-ulonglongtoint8.md) | Converts a value of type ULONGLONG to a value of type INT8. |
| [ULongLongToLong function](..\intsafe\nf-intsafe-ulonglongtolong.md) | Converts a value of type ULONGLONG to a value of type LONG. |
| [ULongLongToLongLong function](..\intsafe\nf-intsafe-ulonglongtolonglong.md) | Converts a value of type ULONGLONG to a value of type INT64. |
| [ULongLongToLongPtr function](..\intsafe\nf-intsafe-ulonglongtolongptr.md) | Converts a value of type ULONGLONG to a value of type LONG_PTR. |
| [ULongLongToShort function](..\intsafe\nf-intsafe-ulonglongtoshort.md) | Converts a value of type ULONGLONG to a value of type SHORT. |
| [ULongLongToUChar function](..\intsafe\nf-intsafe-ulonglongtouchar.md) | Converts a value of type ULONGLONG to a value of type UCHAR. |
| [ULongLongToUInt function](..\intsafe\nf-intsafe-ulonglongtouint.md) | Converts a value of type ULONGLONG to a value of type UINT. |
| [ULongLongToUInt8 function](..\intsafe\nf-intsafe-ulonglongtouint8.md) | Converts a value of type ULONGLONG to a value of type UINT8. |
| [ULongLongToUIntPtr function](..\intsafe\nf-intsafe-ulonglongtouintptr.md) | Converts a value of type ULONGLONG to a value of type size_t. |
| [ULongLongToULong function](..\intsafe\nf-intsafe-ulonglongtoulong.md) | Converts a value of type ULONGLONG to a value of type DWORD. |
| [ULongLongToULongPtr function](..\intsafe\nf-intsafe-ulonglongtoulongptr.md) | Converts a value of type ULONGLONG to a value of type DWORD_PTR. |
| [ULongLongToUShort function](..\intsafe\nf-intsafe-ulonglongtoushort.md) | Converts a value of type ULONGLONG to a value of type USHORT. |
| [ULongMult function](..\intsafe\nf-intsafe-ulongmult.md) | Multiplies one value of type DWORD by another. |
| [ULongPtrAdd function](..\intsafe\nf-intsafe-ulongptradd.md) | Adds two values of type ULONG_PTR. |
| [ULongPtrMult function](..\intsafe\nf-intsafe-ulongptrmult.md) | Multiplies one value of type ULONG_PTR by another. |
| [ULongPtrSub function](..\intsafe\nf-intsafe-ulongptrsub.md) | Subtracts one value of type ULONG_PTR from another. |
| [ULongPtrToChar function](..\intsafe\nf-intsafe-ulongptrtochar.md) | Converts a value of type ULONG_PTR to a value of type CHAR. |
| [ULongPtrToInt function](..\intsafe\nf-intsafe-ulongptrtoint.md) | Converts a value of type size_t to a value of type INT. |
| [ULongPtrToInt8 function](..\intsafe\nf-intsafe-ulongptrtoint8.md) | Converts a value of type ULONG_PTR to a value of type INT8. |
| [ULongPtrToIntPtr function](..\intsafe\nf-intsafe-ulongptrtointptr.md) | Converts a value of type DWORD_PTR to a value of type INT_PTR. |
| [ULongPtrToLong function](..\intsafe\nf-intsafe-ulongptrtolong.md) | Converts a value of type DWORD_PTR to a value of type LONG. |
| [ULongPtrToLongLong function](..\intsafe\nf-intsafe-ulongptrtolonglong.md) | Converts a value of type DWORD_PTR to a value of type INT64. |
| [ULongPtrToLongPtr function](..\intsafe\nf-intsafe-ulongptrtolongptr.md) | Converts a value of type DWORD_PTR to a value of type LONG_PTR. |
| [ULongPtrToShort function](..\intsafe\nf-intsafe-ulongptrtoshort.md) | Converts a value of type ULONG_PTR to a value of type SHORT. |
| [ULongPtrToUChar function](..\intsafe\nf-intsafe-ulongptrtouchar.md) | Converts a value of type ULONG_PTR to a value of type UCHAR. |
| [ULongPtrToUInt function](..\intsafe\nf-intsafe-ulongptrtouint.md) | Converts a value of type DWORD_PTR to a value of type UINT. |
| [ULongPtrToUInt8 function](..\intsafe\nf-intsafe-ulongptrtouint8.md) | Converts a value of type ULONG_PTR to a value of type UINT8. |
| [ULongPtrToUIntPtr function](..\intsafe\nf-intsafe-ulongptrtouintptr.md) | Converts a value of type ULONG_PTR to a value of type UINT_PTR. |
| [ULongPtrToULong function](..\intsafe\nf-intsafe-ulongptrtoulong.md) | Converts a value of type DWORD_PTR to a value of type DWORD. |
| [ULongPtrToUShort function](..\intsafe\nf-intsafe-ulongptrtoushort.md) | Converts a value of type ULONG_PTR to a value of type USHORT. |
| [ULongSub function](..\intsafe\nf-intsafe-ulongsub.md) | Subtracts one value of type DWORD from another. |
| [ULongToChar function](..\intsafe\nf-intsafe-ulongtochar.md) | Converts a value of type DWORD to a value of type CHAR. |
| [ULongToInt function](..\intsafe\nf-intsafe-ulongtoint.md) | Converts a value of type DWORD to a value of type INT. |
| [ULongToInt8 function](..\intsafe\nf-intsafe-ulongtoint8.md) | Converts a value of type ULONG to a value of type INT8. |
| [ULongToIntPtr function](..\intsafe\nf-intsafe-ulongtointptr.md) | Converts a value of type DWORD to a value of type INT_PTR. |
| [ULongToLong function](..\intsafe\nf-intsafe-ulongtolong.md) | Converts a value of type DWORD to a value of type LONG. |
| [ULongToLongPtr function](..\intsafe\nf-intsafe-ulongtolongptr.md) | Converts a value of type DWORD to a value of type LONG_PTR. |
| [ULongToShort function](..\intsafe\nf-intsafe-ulongtoshort.md) | Converts a value of type DWORD to a value of type SHORT. |
| [ULongToUChar function](..\intsafe\nf-intsafe-ulongtouchar.md) | Converts a value of type DWORD to a value of type UCHAR. |
| [ULongToUInt function](..\intsafe\nf-intsafe-ulongtouint.md) | Converts a value of type DWORD to a value of type UINT. |
| [ULongToUInt8 function](..\intsafe\nf-intsafe-ulongtouint8.md) | Converts a value of type DWORD to a value of type BYTE. |
| [ULongToUIntPtr function](..\intsafe\nf-intsafe-ulongtouintptr.md) | Converts a value of type DWORD to a value of type UINT_PTR. |
| [ULongToUShort function](..\intsafe\nf-intsafe-ulongtoushort.md) | Converts a value of type DWORD to a value of type WORD. |
| [URLAssociationDialogA function](..\intshcut\nf-intshcut-urlassociationdialoga.md) | Invokes the unregistered URL protocol dialog box. |
| [URLAssociationDialogW function](..\intshcut\nf-intshcut-urlassociationdialogw.md) | Invokes the unregistered URL protocol dialog box. |
| [UShortAdd function](..\intsafe\nf-intsafe-ushortadd.md) | Adds two values of type USHORT. |
| [UShortMult function](..\intsafe\nf-intsafe-ushortmult.md) | Multiplies one value of type USHORT by another. |
| [UShortSub function](..\intsafe\nf-intsafe-ushortsub.md) | Subtracts one value of type USHORT from another. |
| [UShortToChar function](..\intsafe\nf-intsafe-ushorttochar.md) | Converts a value of type USHORT to a value of type CHAR. |
| [UShortToInt8 function](..\intsafe\nf-intsafe-ushorttoint8.md) | Converts a value of type USHORT to a value of type INT8. |
| [UShortToShort function](..\intsafe\nf-intsafe-ushorttoshort.md) | Converts a value of type USHORT to a value of type SHORT. |
| [UShortToUChar function](..\intsafe\nf-intsafe-ushorttouchar.md) | Converts a value of type USHORT to a value of type BYTE. |
| [UShortToUInt8 function](..\intsafe\nf-intsafe-ushorttouint8.md) | Converts a value of type USHORT to a value of type UINT8. |
| [UnloadUserProfile function](..\userenv\nf-userenv-unloaduserprofile.md) | Unloads a user's profile that was loaded by the LoadUserProfile function. The caller must have administrative privileges on the computer. For more information, see the Remarks section of the LoadUserProfile function. |
| [UnregisterAppStateChangeNotification function](..\appnotify\nf-appnotify-unregisterappstatechangenotification.md) | Cancels a change notification registered through RegisterAppStateChangeNotification. |
| [UrlApplySchemeA function](..\shlwapi\nf-shlwapi-urlapplyschemea.md) | Determines a scheme for a specified URL string, and returns a string with an appropriate prefix. |
| [UrlApplySchemeW function](..\shlwapi\nf-shlwapi-urlapplyschemew.md) | Determines a scheme for a specified URL string, and returns a string with an appropriate prefix. |
| [UrlCanonicalizeA function](..\shlwapi\nf-shlwapi-urlcanonicalizea.md) | Converts a URL string into canonical form. |
| [UrlCanonicalizeW function](..\shlwapi\nf-shlwapi-urlcanonicalizew.md) | Converts a URL string into canonical form. |
| [UrlCombineA function](..\shlwapi\nf-shlwapi-urlcombinea.md) | When provided with a relative URL and its base, returns a URL in canonical form. |
| [UrlCombineW function](..\shlwapi\nf-shlwapi-urlcombinew.md) | When provided with a relative URL and its base, returns a URL in canonical form. |
| [UrlCompareA function](..\shlwapi\nf-shlwapi-urlcomparea.md) | Makes a case-sensitive comparison of two URL strings. |
| [UrlCompareW function](..\shlwapi\nf-shlwapi-urlcomparew.md) | Makes a case-sensitive comparison of two URL strings. |
| [UrlCreateFromPathA function](..\shlwapi\nf-shlwapi-urlcreatefrompatha.md) | Converts a Microsoft MS-DOS path to a canonicalized URL. |
| [UrlCreateFromPathW function](..\shlwapi\nf-shlwapi-urlcreatefrompathw.md) | Converts a Microsoft MS-DOS path to a canonicalized URL. |
| [UrlEscapeA function](..\shlwapi\nf-shlwapi-urlescapea.md) | Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&#0034;unsafe&#0034; characters) into their corresponding escape sequences. |
| [UrlEscapeW function](..\shlwapi\nf-shlwapi-urlescapew.md) | Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&#0034;unsafe&#0034; characters) into their corresponding escape sequences. |
| [UrlFixupW function](..\shlwapi\nf-shlwapi-urlfixupw.md) | UrlFixupW may be altered or unavailable. |
| [UrlGetLocationA function](..\shlwapi\nf-shlwapi-urlgetlocationa.md) | Retrieves the location from a URL. |
| [UrlGetLocationW function](..\shlwapi\nf-shlwapi-urlgetlocationw.md) | Retrieves the location from a URL. |
| [UrlGetPartA function](..\shlwapi\nf-shlwapi-urlgetparta.md) | Accepts a URL string and returns a specified part of that URL. |
| [UrlGetPartW function](..\shlwapi\nf-shlwapi-urlgetpartw.md) | Accepts a URL string and returns a specified part of that URL. |
| [UrlHashA function](..\shlwapi\nf-shlwapi-urlhasha.md) | Hashes a URL string. |
| [UrlHashW function](..\shlwapi\nf-shlwapi-urlhashw.md) | Hashes a URL string. |
| [UrlIsA function](..\shlwapi\nf-shlwapi-urlisa.md) | Tests whether a URL is a specified type. |
| [UrlIsNoHistoryA function](..\shlwapi\nf-shlwapi-urlisnohistorya.md) | Returns whether a URL is a URL that browsers typically do not include in navigation history. |
| [UrlIsNoHistoryW function](..\shlwapi\nf-shlwapi-urlisnohistoryw.md) | Returns whether a URL is a URL that browsers typically do not include in navigation history. |
| [UrlIsOpaqueA function](..\shlwapi\nf-shlwapi-urlisopaquea.md) | Returns whether a URL is opaque. |
| [UrlIsOpaqueW function](..\shlwapi\nf-shlwapi-urlisopaquew.md) | Returns whether a URL is opaque. |
| [UrlIsW function](..\shlwapi\nf-shlwapi-urlisw.md) | Tests whether a URL is a specified type. |
| [UrlUnescapeA function](..\shlwapi\nf-shlwapi-urlunescapea.md) | Converts escape sequences back into ordinary characters. |
| [UrlUnescapeW function](..\shlwapi\nf-shlwapi-urlunescapew.md) | Converts escape sequences back into ordinary characters. |
| [WhichPlatform function](..\shlwapi\nf-shlwapi-whichplatform.md) | WhichPlatform may be altered or unavailable. |
| [Win32DeleteFile function](..\shlobj_core\nf-shlobj_core-win32deletefile.md) | Win32DeleteFile may be altered or unavailable. |
| [WriteCabinetState function](..\shlobj_core\nf-shlobj_core-writecabinetstate.md) | WriteCabinetState may be altered or unavailable. |
| [wnsprintfA function](..\shlwapi\nf-shlwapi-wnsprintfa.md) | Takes a variable-length argument list and returns the values of the arguments as a printf-style formatted string. |
| [wnsprintfW function](..\shlwapi\nf-shlwapi-wnsprintfw.md) | Takes a variable-length argument list and returns the values of the arguments as a printf-style formatted string. |
| [wvnsprintfA function](..\shlwapi\nf-shlwapi-wvnsprintfa.md) | Takes a list of arguments and returns the values of the arguments as a printf-style formatted string. |
| [wvnsprintfW function](..\shlwapi\nf-shlwapi-wvnsprintfw.md) | Takes a list of arguments and returns the values of the arguments as a printf-style formatted string. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [APPLET_PROC callback](..\cpl\nc-cpl-applet_proc.md) | Serves as the entry point for a Control Panel application. This is a library-defined callback function. |
| [DLLGETVERSIONPROC callback function](..\shlwapi\nc-shlwapi-dllgetversionproc.md) | Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information. |
| [LPFNDFMCALLBACK callback](..\shlobj_core\nc-shlobj_core-lpfndfmcallback.md) | LPFNDFMCALLBACK may be altered or unavailable. |
| [LPFNVIEWCALLBACK callback](..\shlobj_core\nc-shlobj_core-lpfnviewcallback.md) | Defines the prototype for the callback function used by the system folder view object. This function essentially duplicates the functionality of IShellFolderViewCB. |
| [PAPPSTATE_CHANGE_ROUTINE callback function](..\appnotify\nc-appnotify-pappstate_change_routine.md) | Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [AUTO_SCROLL_DATA structure](..\shlobj_core\ns-shlobj_core-auto_scroll_data.md) | AUTO_SCROLL_DATA may be altered or unavailable. |
| [BASEBROWSERDATALH structure](..\shdeprecated\ns-shdeprecated-basebrowserdatalh.md) | Contains protected members of the base class. BASEBROWSERDATA defines the browser state and is used with IBrowserService2 |
| [BASEBROWSERDATAXP structure](..\shdeprecated\ns-shdeprecated-basebrowserdataxp.md) | Contains protected members of the base class. BASEBROWSERDATA defines the browser state and is used with IBrowserService2 |
| [CABINETSTATE structure](..\shlobj_core\ns-shlobj_core-cabinetstate.md) | CABINETSTATE may be altered or unavailable. |
| [CONFIRM_CONFLICT_ITEM structure](..\syncmgr\ns-syncmgr-confirm_conflict_item.md) | Defines conflict item structure. |
| [CONFIRM_CONFLICT_RESULT_INFO structure](..\syncmgr\ns-syncmgr-confirm_conflict_result_info.md) | Defines conflict result information structure. |
| [DEFCONTEXTMENU structure](..\shlobj_core\ns-shlobj_core-defcontextmenu.md) | Contains context menu information used by SHCreateDefaultContextMenu. |
| [DFMICS structure](..\shlobj_core\ns-shlobj_core-dfmics.md) | Contains additional arguments used by DFM_INVOKECOMMANDEX. |
| [DROPDESCRIPTION structure](..\shlobj_core\ns-shlobj_core-dropdescription.md) | Describes the image and accompanying text for a drop object. |
| [EXP_DARWIN_LINK structure](..\shlobj_core\ns-shlobj_core-exp_darwin_link.md) | Holds an extra data block used by IShellLinkDataList. It holds the link's Windows Installer ID. |
| [EXP_PROPERTYSTORAGE structure](..\shlobj_core\ns-shlobj_core-exp_propertystorage.md) | Stores information about the Shell link state. This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG. |
| [EXP_SPECIAL_FOLDER structure](..\shlobj_core\ns-shlobj_core-exp_special_folder.md) | Holds an extra data block used by IShellLinkDataList. It holds special folder information. |
| [EXP_SZ_LINK structure](..\shlobj_core\ns-shlobj_core-exp_sz_link.md) | Holds an extra data block used by IShellLinkDataList. It holds expandable environment strings for the icon or target. |
| [FILE_ATTRIBUTES_ARRAY structure](..\shlobj_core\ns-shlobj_core-file_attributes_array.md) | Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY. |
| [NT_CONSOLE_PROPS structure](..\shlobj_core\ns-shlobj_core-nt_console_props.md) | Holds an extra data block used by IShellLinkDataList. It holds console properties. |
| [NT_FE_CONSOLE_PROPS structure](..\shlobj_core\ns-shlobj_core-nt_fe_console_props.md) | Holds an extra data block used by IShellLinkDataList. It holds the console's code page. |
| [QITAB structure](..\shlwapi\ns-shlwapi-qitab.md) | Used by the QISearch function to describe a single interface. |
| [SHARDAPPIDINFO structure](..\shlobj_core\ns-shlobj_core-shardappidinfo.md) | Contains data used by SHAddToRecentDocs to identify both an item&#8212;in this case as an IShellItem&#8212;and the process that it is associated with. |
| [SHARDAPPIDINFOIDLIST structure](..\shlobj_core\ns-shlobj_core-shardappidinfoidlist.md) | Contains data used by SHAddToRecentDocs to identify both an item&#8212;in this case by an absolute pointer to an item identifier list (PIDL)&#8212;and the process that it is associated with. |
| [SHARDAPPIDINFOLINK structure](..\shlobj_core\ns-shlobj_core-shardappidinfolink.md) | Contains data used by SHAddToRecentDocs to identify both an item, in this case through an IShellLink, and the process that it is associated with. |
| [SHELLFLAGSTATE structure](..\shlobj_core\ns-shlobj_core-shellflagstate.md) | Contains a set of flags that indicate the current Shell settings. This structure is used with the SHGetSettings function. |
| [SHFOLDERCUSTOMSETTINGS structure](..\shlobj_core\ns-shlobj_core-shfoldercustomsettings.md) | Holds custom folder settings. This structure is used with the SHGetSetFolderCustomSettings function. |
| [SToolbarItem structure](..\shdeprecated\ns-shdeprecated-stoolbaritem.md) | Deprecated. Data used in IBrowserService2 |
| [SYNCMGR_CONFLICT_ID_INFO structure](..\syncmgr\ns-syncmgr-syncmgr_conflict_id_info.md) | Describes conflict ID information structure. |
| [WTS_THUMBNAILID structure](..\thumbcache\ns-thumbcache-wts_thumbnailid.md) | Contains a unique identifier for a thumbnail in the system thumbnail cache. |
| [_AppInfoData structure](..\shappmgr\ns-shappmgr-_appinfodata.md) | Provides information about a published application to the Add/Remove Programs Control Panel utility. |
| [_COMDLG_FILTERSPEC structure](..\shtypes\ns-shtypes-_comdlg_filterspec.md) | Used generically to filter elements. |
| [_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure](..\credentialprovider\ns-credentialprovider-_credential_provider_credential_serialization.md) | Contains details about a credential. |
| [_CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR structure](..\credentialprovider\ns-credentialprovider-_credential_provider_field_descriptor.md) | Describes a single field in a credential. For example, a string or a user image. |
| [_CSFV structure](..\shlobj_core\ns-shlobj_core-_csfv.md) | Used with the SHCreateShellFolderViewEx function. |
| [_DETAILSINFO structure](..\shlobj_core\ns-shlobj_core-_detailsinfo.md) | Contains detail information for a Shell folder item. Used with the SFVM_GETDETAILSOF notification. |
| [_DLLVERSIONINFO structure](..\shlwapi\ns-shlwapi-_dllversioninfo.md) | Receives DLL-specific version information. |
| [_DLLVERSIONINFO2 structure](..\shlwapi\ns-shlwapi-_dllversioninfo2.md) | Receives DLL-specific version information. It is used with the DllGetVersion function. |
| [_DROPFILES structure](..\shlobj_core\ns-shlobj_core-_dropfiles.md) | Defines the CF_HDROP clipboard format. The data that follows is a double null-terminated list of file names. |
| [_IDA structure](..\shlobj_core\ns-shlobj_core-_ida.md) | Used with the CFSTR_SHELLIDLIST clipboard format to transfer the pointer to an item identifier list (PIDL) of one or more Shell namespace objects. |
| [_ITEMIDLIST structure](..\shtypes\ns-shtypes-_itemidlist.md) | Contains a list of item identifiers. |
| [_ITEMSPACING structure](..\shlobj_core\ns-shlobj_core-_itemspacing.md) | Stores the dimensions of the two possible sizes of icon spacing that are available for display |
| [_NRESARRAY structure](..\shlobj_core\ns-shlobj_core-_nresarray.md) | Defines the CF_NETRESOURCE clipboard format. |
| [_PROFILEINFOA structure](..\profinfo\ns-profinfo-_profileinfoa.md) | Contains information used when loading or unloading a user profile. |
| [_PROFILEINFOW structure](..\profinfo\ns-profinfo-_profileinfow.md) | Contains information used when loading or unloading a user profile. |
| [_PubAppInfo structure](..\shappmgr\ns-shappmgr-_pubappinfo.md) | Provides information about a published application from an application publisher to Add/Remove Programs in Control Panel. |
| [_QCMINFO structure](..\shlobj_core\ns-shlobj_core-_qcminfo.md) | Contains information for merging menu items into Windows Explorer menus. |
| [_SFVM_HELPTOPIC_DATA structure](..\shlobj_core\ns-shlobj_core-_sfvm_helptopic_data.md) | Contains the name of an HTML Help file and a topic in that file. Used with the SFVM_GETHELPTOPIC notification. This structure requires Unicode strings. |
| [_SFVM_PROPPAGE_DATA structure](..\shlobj_core\ns-shlobj_core-_sfvm_proppage_data.md) | Contains the details of a page to be added to an object's Properties sheet. |
| [_SFV_CREATE structure](..\shlobj_core\ns-shlobj_core-_sfv_create.md) | This structure is used with the SHCreateShellFolderView function. |
| [_SHChangeDWORDAsIDList structure](..\shlobj_core\ns-shlobj_core-_shchangedwordasidlist.md) | SHChangeDWORDAsIDList may be altered or unavailable. |
| [_SHChangeNotifyEntry structure](..\shlobj_core\ns-shlobj_core-_shchangenotifyentry.md) | Contains and receives information for change notifications. This structure is used with the SHChangeNotifyRegister function and the SFVM_QUERYFSNOTIFY notification. |
| [_SHChangeUpdateImageIDList structure](..\shlobj_core\ns-shlobj_core-_shchangeupdateimageidlist.md) | SHChangeUpdateImageIDList may be altered or unavailable. |
| [_SHDESCRIPTIONID structure](..\shlobj_core\ns-shlobj_core-_shdescriptionid.md) | Receives item data in response to a call to SHGetDataFromIDList. |
| [_SHELLDETAILS structure](..\shtypes\ns-shtypes-_shelldetails.md) | Reports detailed information on an item in a Shell folder. |
| [_SHITEMID structure](..\shtypes\ns-shtypes-_shitemid.md) | Defines an item identifier. |
| [_STRRET structure](..\shtypes\ns-shtypes-_strret.md) | Contains strings returned from the IShellFolder interface methods. |
| [_WINDOWDATA structure](..\tlogstg\ns-tlogstg-_windowdata.md) | Stores window data. |
| [__MIDL___MIDL_itf_dimm_0000_0000_0003 structure](..\dimm\ns-dimm-__midl___midl_itf_dimm_0000_0000_0003.md) | Defines the attributes of a font. |
| [__MIDL___MIDL_itf_dimm_0000_0000_0004 structure](..\dimm\ns-dimm-__midl___midl_itf_dimm_0000_0000_0004.md) | Defines the attributes of a font. |
| [_browseinfoA structure](..\shlobj_core\ns-shlobj_core-_browseinfoa.md) | Contains parameters for the SHBrowseForFolder function and receives information about the folder selected by the user. |
| [_browseinfoW structure](..\shlobj_core\ns-shlobj_core-_browseinfow.md) | Contains parameters for the SHBrowseForFolder function and receives information about the folder selected by the user. |
| [_openasinfo structure](..\shlobj_core\ns-shlobj_core-_openasinfo.md) | Stores information for the SHOpenWithDialog function. |
| [_tagCOMPONENT structure](..\shlobj_core\ns-shlobj_core-_tagcomponent.md) | Used by Windows 2000 to hold information about a component. This structure replaces the IE4COMPONENT structure. |
| [_tagCOMPONENTSOPT structure](..\shlobj_core\ns-shlobj_core-_tagcomponentsopt.md) | Contains the desktop item options. |
| [_tagCOMPPOS structure](..\shlobj_core\ns-shlobj_core-_tagcomppos.md) | Holds information about a component's position and size. |
| [_tagCOMPSTATEINFO structure](..\shlobj_core\ns-shlobj_core-_tagcompstateinfo.md) | Used by Windows 2000 to hold information about a component's state. |
| [_tagIE4COMPONENT structure](..\shlobj_core\ns-shlobj_core-_tagie4component.md) | Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component. With Windows 2000, it is replaced by the COMPONENT structure. |
| [_tagSYNCMGRHANDLERINFO structure](..\mobsync\ns-mobsync-_tagsyncmgrhandlerinfo.md) | Provides information about the handler for use in the ISyncMgrSynchronize |
| [_tagSYNCMGRITEM structure](..\mobsync\ns-mobsync-_tagsyncmgritem.md) | Provides information about items being enumerated by the ISyncMgrEnumItems interface. |
| [_tagSYNCMGRLOGERRORINFO structure](..\mobsync\ns-mobsync-_tagsyncmgrlogerrorinfo.md) | Provides error information for use in the ISyncMgrSynchronizeCallback |
| [_tagSYNCMGRPROGRESSITEM structure](..\mobsync\ns-mobsync-_tagsyncmgrprogressitem.md) | Provides status information while a synchronization is in progress. This structure is used with the ISyncMgrSynchronizeCallback |
| [_tagSlowAppInfo structure](..\shappmgr\ns-shappmgr-_tagslowappinfo.md) | Provides specialized application information to Add/Remove Programs in Control Panel. This structure is not applicable to published applications. |
| [_tagWALLPAPEROPT structure](..\shlobj_core\ns-shlobj_core-_tagwallpaperopt.md) | Contains the wallpaper display options. Used with members of the IActiveDesktop interface. |
| [tagCPLINFO structure](..\cpl\ns-cpl-tagcplinfo.md) | Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. |
| [tagDATABLOCKHEADER structure](..\shlobj_core\ns-shlobj_core-tagdatablockheader.md) | Serves as the header for some of the extra data structures used by IShellLinkDataList. |
| [tagFolderSetData structure](..\shdeprecated\ns-shdeprecated-tagfoldersetdata.md) | Deprecated. Data used in IBrowserService2 |
| [tagLOGFONTA structure](..\shtypes\ns-shtypes-taglogfonta.md) | Defines the attributes of a font. |
| [tagLOGFONTW structure](..\shtypes\ns-shtypes-taglogfontw.md) | Defines the attributes of a font. |
| [tagNEWCPLINFOA structure](..\cpl\ns-cpl-tagnewcplinfoa.md) | Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. |
| [tagNEWCPLINFOW structure](..\cpl\ns-cpl-tagnewcplinfow.md) | Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. |
| [tagPARSEDURLA structure](..\shlwapi\ns-shlwapi-tagparsedurla.md) | Used by the ParseURL function to return the parsed URL. |
| [tagPARSEDURLW structure](..\shlwapi\ns-shlwapi-tagparsedurlw.md) | Used by the ParseURL function to return the parsed URL. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [ASSOCDATA enumeration](..\shlwapi\ne-shlwapi-assocdata.md) | Used by IQueryAssociations |
| [ASSOCKEY enumeration](..\shlwapi\ne-shlwapi-assockey.md) | Specifies the type of key to be returned by IQueryAssociations |
| [ASSOCSTR enumeration](..\shlwapi\ne-shlwapi-assocstr.md) | Used by IQueryAssociations |
| [CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS enumeration](..\credentialprovider\ne-credentialprovider-credential_provider_account_options.md) | Indicates the type of credential that a credential provider should return to associate with the &#0034;Other user&#0034; tile. Used by ICredentialProviderUserArray_GetAccountOptions. |
| [CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS enumeration](..\credentialprovider\ne-credentialprovider-credential_provider_credential_field_options.md) | Provides customization options for a single field in a logon or credential UI. |
| [DEVICE_SCALE_FACTOR enumeration](..\shtypes\ne-shtypes-device_scale_factor.md) | Indicates a spoofed device scale factor, as a percent. Used by IApplicationDesignModeSettings |
| [DROPIMAGETYPE enumeration](..\shlobj_core\ne-shlobj_core-dropimagetype.md) | Values used with the DROPDESCRIPTION structure to specify the drop image. |
| [FILETYPEATTRIBUTEFLAGS enumeration](..\shlwapi\ne-shlwapi-filetypeattributeflags.md) | Indicates FILETYPEATTRIBUTEFLAGS constants that are used in the EditFlags value of a file association PROGID registry key. |
| [KNOWN_FOLDER_FLAG enumeration](..\shlobj_core\ne-shlobj_core-known_folder_flag.md) | Specify special retrieval options for known folders. These values supersede CSIDL values, which have parallel meanings. |
| [RESTRICTIONS enumeration](..\shlobj_core\ne-shlobj_core-restrictions.md) | These flags are used with the SHRestricted function. |
| [SCNRT_STATUS enumeration](..\shlobj_core\ne-shlobj_core-scnrt_status.md) | Indicates whether to enable or disable Async Register and Deregister for SHChangeNotifyRegisterThread. |
| [SHARD enumeration](..\shlobj_core\ne-shlobj_core-shard.md) | Indicates the interpretation of the data passed by SHAddToRecentDocs in its pv parameter to identify the item whose usage statistics are being tracked. |
| [SHELL_LINK_DATA_FLAGS enumeration](..\shlobj_core\ne-shlobj_core-shell_link_data_flags.md) | Specifies option settings. Used with IShellLinkDataList |
| [SHGLOBALCOUNTER enumeration](..\shlwapi\ne-shlwapi-shglobalcounter.md) | Identifiers for various global counters, or shared variables. Each global counter can be incremented or decremented using SHGlobalCounterIncrement and SHGlobalCounterDecrement. |
| [SHREGDEL_FLAGS enumeration](..\shlwapi\ne-shlwapi-shregdel_flags.md) | Provides a set of values that indicate from which base key an item will be deleted. |
| [SHREGENUM_FLAGS enumeration](..\shlwapi\ne-shlwapi-shregenum_flags.md) | Provides a set of values that indicate the base key that will be used for an enumeration. |
| [SYNCMGR_CANCEL_REQUEST enumeration](..\syncmgr\ne-syncmgr-syncmgr_cancel_request.md) | Describes a request by the user to cancel a synchronization. |
| [SYNCMGR_CONFLICT_ITEM_TYPE enumeration](..\syncmgr\ne-syncmgr-syncmgr_conflict_item_type.md) | Describes conflict item type. |
| [SYNCMGR_CONTROL_FLAGS enumeration](..\syncmgr\ne-syncmgr-syncmgr_control_flags.md) | Specifies how an operation requested on certain methods of ISyncMgrControl should be performed. |
| [SYNCMGR_EVENT_FLAGS enumeration](..\syncmgr\ne-syncmgr-syncmgr_event_flags.md) | Specifies flags for a synchronization event. |
| [SYNCMGR_EVENT_LEVEL enumeration](..\syncmgr\ne-syncmgr-syncmgr_event_level.md) | Specifies the type of event being reported to Sync Center. |
| [SYNCMGR_HANDLER_CAPABILITIES enumeration](..\syncmgr\ne-syncmgr-syncmgr_handler_capabilities.md) | Specifies the capabilities of a handler regarding the actions that can be performed against it. |
| [SYNCMGR_HANDLER_POLICIES enumeration](..\syncmgr\ne-syncmgr-syncmgr_handler_policies.md) | Enumerates policies specified by a sync handler that deviate from the default policy. |
| [SYNCMGR_HANDLER_TYPE enumeration](..\syncmgr\ne-syncmgr-syncmgr_handler_type.md) | Specifies the type of a handler. Used by ISyncMgrHandlerInfo |
| [SYNCMGR_ITEM_CAPABILITIES enumeration](..\syncmgr\ne-syncmgr-syncmgr_item_capabilities.md) | Specifies the actions that can be performed against an item. |
| [SYNCMGR_ITEM_POLICIES enumeration](..\syncmgr\ne-syncmgr-syncmgr_item_policies.md) | Specifies an item's policies to control how they can be enabled or disabled by group policy. |
| [SYNCMGR_PRESENTER_CHOICE enumeration](..\syncmgr\ne-syncmgr-syncmgr_presenter_choice.md) | Describes what choice a user makes about a sync manager conflict resolution. Used by ISyncMgrConflictPresenter. |
| [SYNCMGR_PRESENTER_NEXT_STEP enumeration](..\syncmgr\ne-syncmgr-syncmgr_presenter_next_step.md) | Describes the next step that is to occur in sync manager conflict resolution. Used by ISyncMgrConflictPresenter. |
| [SYNCMGR_PROGRESS_STATUS enumeration](..\syncmgr\ne-syncmgr-syncmgr_progress_status.md) | Specifies the current progress status of a synchronization process. Used by ISyncMgrSyncCallback |
| [SYNCMGR_RESOLUTION_ABILITIES enumeration](..\syncmgr\ne-syncmgr-syncmgr_resolution_abilities.md) | Indicates abilities and the conflict resolution activity to follow. Used with ISyncMgrResolutionHandler |
| [SYNCMGR_RESOLUTION_FEEDBACK enumeration](..\syncmgr\ne-syncmgr-syncmgr_resolution_feedback.md) | Describes Sync Manager resolution feedback. Used by ISyncMgrResolutionHandler. |
| [SYNCMGR_SYNC_CONTROL_FLAGS enumeration](..\syncmgr\ne-syncmgr-syncmgr_sync_control_flags.md) | Indicates flags used by ISyncMgrControl |
| [ThumbnailStreamCacheOptions enumeration](..\thumbnailstreamcache\ne-thumbnailstreamcache-thumbnailstreamcacheoptions.md) | Defines the cache options used by the IThumbnailStreamCache interface. |
| [URL_SCHEME enumeration](..\shlwapi\ne-shlwapi-url_scheme.md) | Used to specify URL schemes. |
| [WTS_CONTEXTFLAGS enumeration](..\thumbcache\ne-thumbcache-wts_contextflags.md) | Specifies the context of a thumbnail extraction. Used by IThumbnailSettings |
| [WTS_FLAGS enumeration](..\thumbcache\ne-thumbcache-wts_flags.md) | Values used by IThumbnailCache |
| [_CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_field_interactive_state.md) | Describes the state of a field and how it a user can interact with it. Fields can be displayed by a credential provider in a variety of different interactive states. |
| [_CREDENTIAL_PROVIDER_FIELD_STATE enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_field_state.md) | Specifies the state of a single field in the Credential UI. |
| [_CREDENTIAL_PROVIDER_FIELD_TYPE enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_field_type.md) | Specifies a type of credential field. Used by CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR. |
| [_CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_get_serialization_response.md) | Describes the response when a credential provider attempts to serialize credentials. |
| [_CREDENTIAL_PROVIDER_STATUS_ICON enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_status_icon.md) | Indicates which status icon should be displayed. |
| [_CREDENTIAL_PROVIDER_USAGE_SCENARIO enumeration](..\credentialprovider\ne-credentialprovider-_credential_provider_usage_scenario.md) | Declares the scenarios in which a credential provider is supported. A credential provider usage scenario (CPUS) enables the credential provider to provide distinct enumeration behavior and UI field setup across scenarios. |
| [_tagAUTOCOMPLETELISTOPTIONS enumeration](..\shlobj_core\ne-shlobj_core-_tagautocompletelistoptions.md) | Specifies which objects are enumerated for autocompletion lists. |
| [_tagAppActionFlags enumeration](..\shappmgr\ne-shappmgr-_tagappactionflags.md) | Specifies application management actions supported by an application publisher. These flags are bitmasks passed to IShellApp |
| [_tagAppInfoFlags enumeration](..\shappmgr\ne-shappmgr-_tagappinfoflags.md) | Specifies application information to return from IShellApp |
| [_tagPublishedAppInfoFlags enumeration](..\shappmgr\ne-shappmgr-_tagpublishedappinfoflags.md) | Specifies which members in the PUBAPPINFO structure are valid. These flags are bitmasks set in the dwMask member and passed to IPublishedApp |
| [_tagSYNCMGRFLAG enumeration](..\mobsync\ne-mobsync-_tagsyncmgrflag.md) | The SYNCMGRFLAG enumeration values are used in the ISyncMgrSynchronize |
| [_tagSYNCMGRHANDLERFLAGS enumeration](..\mobsync\ne-mobsync-_tagsyncmgrhandlerflags.md) | Used in the SYNCMGRHANDLERINFO structure as flags that apply to the current handler. |
| [_tagSYNCMGRINVOKEFLAGS enumeration](..\mobsync\ne-mobsync-_tagsyncmgrinvokeflags.md) | The SYNCMGRINVOKEFLAGS enumeration value specifies how the Sync Manager is to be invoked in the ISyncMgrSynchronizeInvoke |
| [_tagSYNCMGRITEMFLAGS enumeration](..\mobsync\ne-mobsync-_tagsyncmgritemflags.md) | Specifies information for the current item in the SYNCMGRITEM structure. |
| [_tagSYNCMGRLOGLEVEL enumeration](..\mobsync\ne-mobsync-_tagsyncmgrloglevel.md) | The SYNCMGRLOGLEVEL enumeration values specify an error level for use in the ISyncMgrSynchronizeCallback |
| [_tagSYNCMGRREGISTERFLAGS enumeration](..\mobsync\ne-mobsync-_tagsyncmgrregisterflags.md) | The SYNCMGRREGISTERFLAGS enumeration values are used in methods of the ISyncMgrRegister interface to identify events for which the handler is registered to be notified. |
| [_tagSYNCMGRSTATUS enumeration](..\mobsync\ne-mobsync-_tagsyncmgrstatus.md) | Used in the ISyncMgrSynchronize |
| [mimeassociationdialog_in_flags enumeration](..\intshcut\ne-intshcut-mimeassociationdialog_in_flags.md) | Used with the MIMEAssociationDialog function to determine how it executes. |
| [tagBNSTATE enumeration](..\shdeprecated\ne-shdeprecated-tagbnstate.md) | Deprecated. Used by IBrowserService |
| [tagIESHORTCUTFLAGS enumeration](..\shlobj_core\ne-shlobj_core-tagieshortcutflags.md) | Specifies how a shortcut should be handled by the browser. |
| [tagPERCEIVED enumeration](..\shtypes\ne-shtypes-tagperceived.md) | Specifies a file's perceived type. This set of constants is used in the AssocGetPerceivedType function. |
| [tagSFBS_FLAGS enumeration](..\shlwapi\ne-shlwapi-tagsfbs_flags.md) | Specifies how the StrFormatByteSizeEx function should handle rounding of undisplayed digits. |
| [tagSHCOLSTATE enumeration](..\shtypes\ne-shtypes-tagshcolstate.md) | Describes how a property should be treated. These values are defined in Shtypes.h. |
| [translateurl_in_flags enumeration](..\intshcut\ne-intshcut-translateurl_in_flags.md) | The TRANSLATEURL_IN_FLAGS enumerated values are used with the TranslateURL function to determine how it will execute. |
| [urlassociationdialog_in_flags enumeration](..\intshcut\ne-intshcut-urlassociationdialog_in_flags.md) | The URLASSOCIATIONDIALOG_IN_FLAGS enumerated values are used with URLAssociationDialog to determine how it executes. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IAppPublisher interface](..\shappmgr\nn-shappmgr-iapppublisher.md) | Exposes methods for publishing applications through Add/Remove Programs in Control Panel. This is the principal interface implemented for this purpose. |
| [IBrowserService interface](..\shdeprecated\nn-shdeprecated-ibrowserservice.md) | Deprecated. |
| [IBrowserService2 interface](..\shdeprecated\nn-shdeprecated-ibrowserservice2.md) | Deprecated. |
| [IBrowserService3 interface](..\shdeprecated\nn-shdeprecated-ibrowserservice3.md) | Deprecated. |
| [IBrowserService4 interface](..\shdeprecated\nn-shdeprecated-ibrowserservice4.md) | Deprecated. |
| [IConnectableCredentialProviderCredential interface](..\credentialprovider\nn-credentialprovider-iconnectablecredentialprovidercredential.md) | Exposes methods for connecting and disconnecting IConnectableCredentialProviderCredential objects. |
| [ICredentialProvider interface](..\credentialprovider\nn-credentialprovider-icredentialprovider.md) | Exposes methods used in the setup and manipulation of a credential provider. All credential providers must implement this interface. |
| [ICredentialProviderCredential interface](..\credentialprovider\nn-credentialprovider-icredentialprovidercredential.md) | Exposes methods that enable the handling of a credential. |
| [ICredentialProviderCredential2 interface](..\credentialprovider\nn-credentialprovider-icredentialprovidercredential2.md) | Extends the ICredentialProviderCredential interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile. |
| [ICredentialProviderCredentialEvents interface](..\credentialprovider\nn-credentialprovider-icredentialprovidercredentialevents.md) | Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI. |
| [ICredentialProviderCredentialEvents2 interface](..\credentialprovider\nn-credentialprovider-icredentialprovidercredentialevents2.md) | Extends the ICredentialProviderCredentialEvents interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI. |
| [ICredentialProviderCredentialWithFieldOptions interface](..\credentialprovider\nn-credentialprovider-icredentialprovidercredentialwithfieldoptions.md) | Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI. |
| [ICredentialProviderEvents interface](..\credentialprovider\nn-credentialprovider-icredentialproviderevents.md) | Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields. |
| [ICredentialProviderFilter interface](..\credentialprovider\nn-credentialprovider-icredentialproviderfilter.md) | Used to dynamically filter credential providers based on information available at runtime. |
| [ICredentialProviderSetUserArray interface](..\credentialprovider\nn-credentialprovider-icredentialprovidersetuserarray.md) | Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI. |
| [ICredentialProviderUser interface](..\credentialprovider\nn-credentialprovider-icredentialprovideruser.md) | Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI. |
| [ICredentialProviderUserArray interface](..\credentialprovider\nn-credentialprovider-icredentialprovideruserarray.md) | Represents the set of users that will appear in the logon or credential UI. This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set. |
| [IEnumPublishedApps interface](..\shappmgr\nn-shappmgr-ienumpublishedapps.md) | Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through IAppPublisher |
| [IEnumSyncMgrConflict interface](..\syncmgr\nn-syncmgr-ienumsyncmgrconflict.md) | Exposes conflict enumeration methods. |
| [IEnumSyncMgrEvents interface](..\syncmgr\nn-syncmgr-ienumsyncmgrevents.md) | Exposes sync event enumeration methods. |
| [IEnumSyncMgrSyncItems interface](..\syncmgr\nn-syncmgr-ienumsyncmgrsyncitems.md) | Exposes methods that enumerate the sync item objects managed by the handler. |
| [IExpDispSupport interface](..\shdeprecated\nn-shdeprecated-iexpdispsupport.md) | Deprecated. Exposes methods that allow the retrieval of properties, translation of keyboard accelerators, and determination of a connection point for certain events. |
| [IExpDispSupportXP interface](..\shdeprecated\nn-shdeprecated-iexpdispsupportxp.md) | Deprecated. Exposes methods that allow the retrieval of properties, translation of keyboard accelerators, and determination of a connection point for certain events. |
| [IInputPanelConfiguration interface](..\inputpanelconfiguration\nn-inputpanelconfiguration-iinputpanelconfiguration.md) | Provides functionality for desktop apps to opt in to the focus tracking mechanism used in Windows Store apps. |
| [IInputPanelInvocationConfiguration interface](..\inputpanelconfiguration\nn-inputpanelconfiguration-iinputpanelinvocationconfiguration.md) | Enables Windows Store apps to opt out of the automatic invocation behavior. |
| [IObjectArray interface](..\objectarray\nn-objectarray-iobjectarray.md) | Exposes methods that enable clients to access items in a collection of objects that support IUnknown. |
| [IObjectCollection interface](..\objectarray\nn-objectarray-iobjectcollection.md) | Extends the IObjectArray interface by providing methods that enable clients to add and remove objects that support IUnknown in a collection. |
| [IPublishedApp interface](..\shappmgr\nn-shappmgr-ipublishedapp.md) | Exposes methods that represent applications to Add/Remove Programs in Control Panel. |
| [IPublishedApp2 interface](..\shappmgr\nn-shappmgr-ipublishedapp2.md) | Extends the IPublishedApp interface by providing an additional installation method. |
| [IQueryContinueWithStatus interface](..\credentialprovider\nn-credentialprovider-iquerycontinuewithstatus.md) | Exposes methods that provide a standard mechanism for credential providers to call QueryContinue while attempting to connect to the network to determine if they should continue these attempts. |
| [ISharedBitmap interface](..\thumbcache\nn-thumbcache-isharedbitmap.md) | Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed. |
| [IShellApp interface](..\shappmgr\nn-shappmgr-ishellapp.md) | Exposes methods that provide general information about an application to the Add/Remove Programs Application. |
| [IShellImageData interface](..\shimgdata\nn-shimgdata-ishellimagedata.md) | Exposes methods and properties that display, manipulate, and describe image data. |
| [IShellImageDataAbort interface](..\shimgdata\nn-shimgdata-ishellimagedataabort.md) | Exposes a single method used to abort IShellImageData processes. |
| [IShellImageDataFactory interface](..\shimgdata\nn-shimgdata-ishellimagedatafactory.md) | Exposes methods that create IShellImageData instances based on various image sources. |
| [IShellService interface](..\shdeprecated\nn-shdeprecated-ishellservice.md) | Deprecated. IShellService Exposes one method that declares ownership when a service component implementing a certain interface is shared among multiple clients, such as Windows Internet Explorer and Windows Explorer. |
| [IStorageProviderHandler interface](..\storageprovider\nn-storageprovider-istorageproviderhandler.md) | Retrieves the IStorageProviderPropertyHandler associated with a specific file or folder. |
| [IStorageProviderPropertyHandler interface](..\storageprovider\nn-storageprovider-istorageproviderpropertyhandler.md) | Provides a collection of properties associated with a file or folder. |
| [ISyncMgrConflict interface](..\syncmgr\nn-syncmgr-isyncmgrconflict.md) | Exposes methods that provide information about a conflict retrieved from a conflict store, and allows the conflict to be resolved. |
| [ISyncMgrConflictFolder interface](..\syncmgr\nn-syncmgr-isyncmgrconflictfolder.md) | Exposes a method that gets the conflict ID list for a conflict object. |
| [ISyncMgrConflictItems interface](..\syncmgr\nn-syncmgr-isyncmgrconflictitems.md) | Exposes methods that get conflict item data and item count. |
| [ISyncMgrConflictPresenter interface](..\syncmgr\nn-syncmgr-isyncmgrconflictpresenter.md) | Exposes a method that presents a conflict to the user. |
| [ISyncMgrConflictResolutionItems interface](..\syncmgr\nn-syncmgr-isyncmgrconflictresolutionitems.md) | Exposes methods that get item info and item count. |
| [ISyncMgrConflictResolveInfo interface](..\syncmgr\nn-syncmgr-isyncmgrconflictresolveinfo.md) | Exposes methods that get and set information about sync manager conflict resolution. |
| [ISyncMgrConflictStore interface](..\syncmgr\nn-syncmgr-isyncmgrconflictstore.md) | Exposes methods that allow a handler to provide conflicts that appear in the Conflicts folder. |
| [ISyncMgrControl interface](..\syncmgr\nn-syncmgr-isyncmgrcontrol.md) | Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values. |
| [ISyncMgrEnumItems interface](..\mobsync\nn-mobsync-isyncmgrenumitems.md) | Exposes methods that enumerate through an array of SYNCMGRITEM structures. |
| [ISyncMgrEvent interface](..\syncmgr\nn-syncmgr-isyncmgrevent.md) | Exposes methods that retrieve data from an event store. An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events. |
| [ISyncMgrEventLinkUIOperation interface](..\syncmgr\nn-syncmgr-isyncmgreventlinkuioperation.md) | Provides a method that is called when event links are clicked in the sync results folder. |
| [ISyncMgrEventStore interface](..\syncmgr\nn-syncmgr-isyncmgreventstore.md) | Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store. These events are displayed in the Sync Results folder. |
| [ISyncMgrHandler interface](..\syncmgr\nn-syncmgr-isyncmgrhandler.md) | Exposes methods that make up the primary interface implemented by a sync handler. |
| [ISyncMgrHandlerCollection interface](..\syncmgr\nn-syncmgr-isyncmgrhandlercollection.md) | Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers. |
| [ISyncMgrHandlerInfo interface](..\syncmgr\nn-syncmgr-isyncmgrhandlerinfo.md) | Exposes methods that allow a handler to provide property and state information to Sync Center. |
| [ISyncMgrRegister interface](..\mobsync\nn-mobsync-isyncmgrregister.md) | Exposes methods so that an application can register with the synchronization manager. This can be achieved either through the ISyncMgrRegister interface or by registering directly in the registry. |
| [ISyncMgrResolutionHandler interface](..\syncmgr\nn-syncmgr-isyncmgrresolutionhandler.md) | Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user. |
| [ISyncMgrScheduleWizardUIOperation interface](..\syncmgr\nn-syncmgr-isyncmgrschedulewizarduioperation.md) | Exposes a method that allows a handler to display the sync schedule wizard for the handler. |
| [ISyncMgrSessionCreator interface](..\syncmgr\nn-syncmgr-isyncmgrsessioncreator.md) | Exposes a single method through which a handler or external application can notify Sync Center that synchronization has begun, as well as report progress and events. |
| [ISyncMgrSyncCallback interface](..\syncmgr\nn-syncmgr-isyncmgrsynccallback.md) | Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled. |
| [ISyncMgrSyncItem interface](..\syncmgr\nn-syncmgr-isyncmgrsyncitem.md) | Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects. |
| [ISyncMgrSyncItemContainer interface](..\syncmgr\nn-syncmgr-isyncmgrsyncitemcontainer.md) | Exposes methods that provide information to handlers about the items they contain. |
| [ISyncMgrSyncItemInfo interface](..\syncmgr\nn-syncmgr-isyncmgrsynciteminfo.md) | Exposes methods that provide property and state information for a single sync item. |
| [ISyncMgrSyncResult interface](..\syncmgr\nn-syncmgr-isyncmgrsyncresult.md) | Exposes a method that applications calling ISyncMgrControl can use to get the result of a ISyncMgrControl |
| [ISyncMgrSynchronize interface](..\mobsync\nn-mobsync-isyncmgrsynchronize.md) | Exposes methods that enable the registered application or service to receive notifications from the synchronization manager. |
| [ISyncMgrSynchronizeCallback interface](..\mobsync\nn-mobsync-isyncmgrsynchronizecallback.md) | Exposes methods that manage the synchronization process. |
| [ISyncMgrSynchronizeInvoke interface](..\mobsync\nn-mobsync-isyncmgrsynchronizeinvoke.md) | Exposes methods that enable a registered application to invoke the synchronization manager to update items. |
| [ISyncMgrUIOperation interface](..\syncmgr\nn-syncmgr-isyncmgruioperation.md) | Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center. |
| [IThumbnailCache interface](..\thumbcache\nn-thumbcache-ithumbnailcache.md) | Exposes methods for a system thumbnail cache that is shared across applications. |
| [IThumbnailProvider interface](..\thumbcache\nn-thumbcache-ithumbnailprovider.md) | Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers. The object that implements this interface must also implement IInitializeWithStream. |
| [IThumbnailSettings interface](..\thumbcache\nn-thumbcache-ithumbnailsettings.md) | Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request. |
| [IThumbnailStreamCache interface](..\thumbnailstreamcache\nn-thumbnailstreamcache-ithumbnailstreamcache.md) | Gets or sets the thumbnail stream. This interface is for internal use only and can only be called by the photos application. |
| [ITrackShellMenu interface](..\shdeprecated\nn-shdeprecated-itrackshellmenu.md) | Exposes methods that extend the IShellMenu interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu. |
| [ITranscodeImage interface](..\imagetranscode\nn-imagetranscode-itranscodeimage.md) | Exposes a method that allows conversion to JPEG or bitmap (BMP) image formats from any image type supported by Windows. |
| [ITravelEntry interface](..\shdeprecated\nn-shdeprecated-itravelentry.md) | Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history. |
| [ITravelLog interface](..\shdeprecated\nn-shdeprecated-itravellog.md) | Deprecated. Exposes methods that maintain and manipulate a record of travel in the browser. |

## Classes

| Title   | Description   |
| ---- |:---- |
| [CItemIDFactory class](..\shidfact\nl-shidfact-citemidfactory.md) | Exposes methods for interacting with Shell data sources. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [DEFINE_PROPERTYKEY macro](..\propkeydef\nf-propkeydef-define_propertykey.md) | Used to pack a format identifier (FMTID) and property identifier (PID) into a PROPERTYKEY structure that represents a property key. |
| [IntlStrEqNA macro](..\shlwapi\nf-shlwapi-intlstreqna.md) | Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings. |
| [IntlStrEqNIA macro](..\shlwapi\nf-shlwapi-intlstreqnia.md) | Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings. |
| [IntlStrEqNIW macro](..\shlwapi\nf-shlwapi-intlstreqniw.md) | Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings. |
| [IntlStrEqNW macro](..\shlwapi\nf-shlwapi-intlstreqnw.md) | Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings. |
| [IsEqualPropertyKey macro](..\propkeydef\nf-propkeydef-isequalpropertykey.md) | Compares the members of two PROPERTYKEY structures and returns whether they are equal. |
| [MAKEDLLVERULL macro](..\shlwapi\nf-shlwapi-makedllverull.md) | Used to pack DLL version information into a ULONGLONG value. |
| [PathIsHTMLFileA macro](..\shlwapi\nf-shlwapi-pathishtmlfilea.md) | Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension. |
| [PathIsHTMLFileW macro](..\shlwapi\nf-shlwapi-pathishtmlfilew.md) | Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension. |
| [UrlEscapeSpaces macro](..\shlwapi\nf-shlwapi-urlescapespaces.md) | A macro that converts space characters into their corresponding escape sequence. |
| [UrlIsFileUrlA macro](..\shlwapi\nf-shlwapi-urlisfileurla.md) | Tests a URL to determine if it is a file URL. |
| [UrlIsFileUrlW macro](..\shlwapi\nf-shlwapi-urlisfileurlw.md) | Tests a URL to determine if it is a file URL. |
| [UrlUnescapeInPlace macro](..\shlwapi\nf-shlwapi-urlunescapeinplace.md) | Converts escape sequences back into ordinary characters and overwrites the original string. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [CItemIDFactory::CreateItemID](..\shidfact\nf-shidfact-citemidfactory-createitemid.md) | Creates an ItemID from the supplied data. |
| [CItemIDFactory::GetDataFromIDList method](..\shidfact\nf-shidfact-citemidfactory-getdatafromidlist.md) | Gets a read only pointer to the client provided structure in the first ItemID in the IDList. |
| [CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE)](..\shidfact\nf-shidfact-citemidfactory-getdatafromidlist(pcuidlist_relative).md) | Gets a read only pointer to the client provided structure in the first ItemID in the IDList. |
| [CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE,const T)](..\shidfact\nf-shidfact-citemidfactory-getdatafromidlist(pcuidlist_relative,const t).md) | Gets a read only pointer to the client provided structure in the first ItemID in the IDList. |
| [CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)](..\shidfact\nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative,pcwstr,propvariant).md) | Gets a property from the IPropertyStore within the IDList as a variant, using the key. |
| [CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT)](..\shidfact\nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative,pcwstr,variant).md) | Gets a property from the IPropertyStore within the IDList as a variant, using the key. |
| [CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,REFPROPERTYKEY,PROPVARIANT)](..\shidfact\nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative,refpropertykey,propvariant).md) | Gets a property from the IPropertyStore within the IDList as a variant, using the key. |
| [CItemIDFactory::GetPropertyFromIDList](..\shidfact\nf-shidfact-citemidfactory-getpropertyfromidlist.md) | Gets a property from the IPropertyStore within the IDList as a variant, using the key. |
| [CItemIDFactory::GetPropertyStorageFromIDList](..\shidfact\nf-shidfact-citemidfactory-getpropertystoragefromidlist.md) | Create an instance of the IPropertyStore based on the serialized property storage associated with the first ItemID. |
| [CItemIDFactory::GetPropertyStorage](..\shidfact\nf-shidfact-citemidfactory-getpropertystorage.md) | Gets a read only pointer to the serialized property storage that is used for storing metadata. |
| [CItemIDFactory::IsDelegateFolder](..\shidfact\nf-shidfact-citemidfactory-isdelegatefolder.md) | Gets a Boolean value specifying whether the factory is a delegate folder. |
| [CItemIDFactory::SetItemAlloc](..\shidfact\nf-shidfact-citemidfactory-setitemalloc.md) | Provides the CItemIDFactory an IMalloc interface used to allocate and free item IDs. |
| [IAppPublisher::EnumApps](..\shappmgr\nf-shappmgr-iapppublisher-enumapps.md) | Creates an enumerator for enumerating all applications published by an application publisher for a given category. |
| [IAppPublisher::GetCategories](..\shappmgr\nf-shappmgr-iapppublisher-getcategories.md) | Retrieves a structure listing the categories provided by an application publisher. |
| [IAppPublisher::GetNumberOfApps](..\shappmgr\nf-shappmgr-iapppublisher-getnumberofapps.md) | Obsolete. Clients of Add/Remove Programs Control Panel Application can return E_NOTIMPL. |
| [IAppPublisher::GetNumberOfCategories](..\shappmgr\nf-shappmgr-iapppublisher-getnumberofcategories.md) | Obsolete. Clients of the Add/Remove Programs Control Panel Application may return E_NOTIMPL. |
| [IBrowserService2::ActivatePendingView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-activatependingview.md) | Deprecated. Coordinates state updating while the browser is switching between a current and a pending view. |
| [IBrowserService2::AllowViewResize](..\shdeprecated\nf-shdeprecated-ibrowserservice2-allowviewresize.md) | Deprecated. Informs the base class whether to allow view resizing. |
| [IBrowserService2::CreateBrowserPropSheetExt](..\shdeprecated\nf-shdeprecated-ibrowserservice2-createbrowserpropsheetext.md) | Deprecated. Allows the derived class to add Folder Options property sheets to the base class. |
| [IBrowserService2::CreateViewWindow](..\shdeprecated\nf-shdeprecated-ibrowserservice2-createviewwindow.md) | Deprecated. Coordinates the updating of state when creating a new browser view window. |
| [IBrowserService2::ForwardViewMsg](..\shdeprecated\nf-shdeprecated-ibrowserservice2-forwardviewmsg.md) | Deprecated. Calls the SendMessage function with a message received by the view, using the _hwndView member of the BASEBROWSERDATA structure as the SendMessage hWnd parameter. |
| [IBrowserService2::GetBaseBrowserData](..\shdeprecated\nf-shdeprecated-ibrowserservice2-getbasebrowserdata.md) | Deprecated. Gets a read-only structure containing the protected elements owned by the base class, for the purpose of determining state. |
| [IBrowserService2::GetFolderSetData](..\shdeprecated\nf-shdeprecated-ibrowserservice2-getfoldersetdata.md) | Deprecated. Gets a structure containing folder information. |
| [IBrowserService2::GetViewRect](..\shdeprecated\nf-shdeprecated-ibrowserservice2-getviewrect.md) | Deprecated. Retrieves a value that is used to negotiate the allowed size of the window. |
| [IBrowserService2::GetViewWindow](..\shdeprecated\nf-shdeprecated-ibrowserservice2-getviewwindow.md) | Deprecated. Provides direct access to the browser view window created by IBrowserService2 |
| [IBrowserService2::InitializeDownloadManager](..\shdeprecated\nf-shdeprecated-ibrowserservice2-initializedownloadmanager.md) | Deprecated. Enables the download manager in the base class. |
| [IBrowserService2::InitializeTransitionSite](..\shdeprecated\nf-shdeprecated-ibrowserservice2-initializetransitionsite.md) | Deprecated. Enables transitions in the browser view window. |
| [IBrowserService2::InitializeTravelLog](..\shdeprecated\nf-shdeprecated-ibrowserservice2-initializetravellog.md) | Deprecated. Allows the derived class to specify a navigation record to be used in a new window. |
| [IBrowserService2::Offline](..\shdeprecated\nf-shdeprecated-ibrowserservice2-offline.md) | Deprecated. Checks for and updates the browser's offline status, synchronzing the state between the base class and any derived classes. |
| [IBrowserService2::OnCommand](..\shdeprecated\nf-shdeprecated-ibrowserservice2-oncommand.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_COMMAND message. The derived class handles the message. |
| [IBrowserService2::OnCreate](..\shdeprecated\nf-shdeprecated-ibrowserservice2-oncreate.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_CREATE message. The derived class handles the message. |
| [IBrowserService2::OnDestroy](..\shdeprecated\nf-shdeprecated-ibrowserservice2-ondestroy.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_DESTROY message. The derived class handles the message. |
| [IBrowserService2::OnFrameWindowActivateBS](..\shdeprecated\nf-shdeprecated-ibrowserservice2-onframewindowactivatebs.md) | Deprecated. Calls the derived class from the base class in response to a subframe window being activated or deactivated. The derived class determines what to do in response to the action. |
| [IBrowserService2::OnNotify](..\shdeprecated\nf-shdeprecated-ibrowserservice2-onnotify.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_NOTIFY message. The derived class handles the message. |
| [IBrowserService2::OnSetFocus](..\shdeprecated\nf-shdeprecated-ibrowserservice2-onsetfocus.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_SETFOCUS message. The derived class handles the message. |
| [IBrowserService2::OnSize](..\shdeprecated\nf-shdeprecated-ibrowserservice2-onsize.md) | Deprecated. Calls the derived class from the base class on receipt of a WM_SIZE message. The derived class handles the message. |
| [IBrowserService2::PutBaseBrowserData](..\shdeprecated\nf-shdeprecated-ibrowserservice2-putbasebrowserdata.md) | Deprecated. Gets a structure that allows read/write access to protected members of the base class. Note, however, that state should only be updated by the base browser. |
| [IBrowserService2::ReleaseShellView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-releaseshellview.md) | Deprecated. Coordinates the view lifetime between the base class and its derived class. |
| [IBrowserService2::SetAcceleratorMenu](..\shdeprecated\nf-shdeprecated-ibrowserservice2-setacceleratormenu.md) | Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to TranslateAcceleratorSB. |
| [IBrowserService2::SetActivateState](..\shdeprecated\nf-shdeprecated-ibrowserservice2-setactivatestate.md) | Deprecated. Updates the value of the _uActivateState member of the BASEBROWSERDATA structure, which tracks whether the browser view window is in an activated state. The derived class makes this call to the base class. |
| [IBrowserService2::SetAsDefFolderSettings](..\shdeprecated\nf-shdeprecated-ibrowserservice2-setasdeffoldersettings.md) | Deprecated. Sets the folder's current view mode as the default view mode for all folders. Used by the Folder Options dialog. |
| [IBrowserService2::SetTopBrowser](..\shdeprecated\nf-shdeprecated-ibrowserservice2-settopbrowser.md) | Deprecated. Informs the base class when it becomes the topmost browser instance. |
| [IBrowserService2::UpdateSecureLockIcon](..\shdeprecated\nf-shdeprecated-ibrowserservice2-updatesecurelockicon.md) | Deprecated. Updates the value of the _eSecureLockIcon member of the BASEBROWSERDATA structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI. |
| [IBrowserService2::WndProcBS](..\shdeprecated\nf-shdeprecated-ibrowserservice2-wndprocbs.md) | Deprecated. Allows a derived class to call the WinProc function of the base class. |
| [IBrowserService2::_CancelPendingNavigationAsync](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_cancelpendingnavigationasync.md) | Deprecated. Enables a derived class to request that the base class cancel any pending navigation. |
| [IBrowserService2::_CancelPendingView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_cancelpendingview.md) | Deprecated. Enables a derived class to request that the base class cancel any pending views. |
| [IBrowserService2::_CloseAndReleaseToolbars](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_closeandreleasetoolbars.md) | Deprecated. Requests the closing of the browser toolbars hosted by the derived class. |
| [IBrowserService2::_DisableModeless](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_disablemodeless.md) | Deprecated. Enables a derived class to ask the base class whether a modal UI is visible. A modal UI blocks minimize and close behavior in the browser window. |
| [IBrowserService2::_ExecChildren](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_execchildren.md) | Deprecated. Enables the derived class to issue a command through the IOleCommandTarget |
| [IBrowserService2::_FindTBar](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_findtbar.md) | Deprecated. Returns the index of a browser toolbar item based on Component Object Model (COM) identity rules. |
| [IBrowserService2::_GetBorderDWHelper](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_getborderdwhelper.md) | Deprecated. A helper method for the implementation of GetBorderDW. |
| [IBrowserService2::_GetEffectiveClientArea](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_geteffectiveclientarea.md) | Deprecated. Used with IBrowserService2 |
| [IBrowserService2::_GetToolbarCount](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_gettoolbarcount.md) | Deprecated. Returns the number of toolbars in the browser window. |
| [IBrowserService2::_GetToolbarItem](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_gettoolbaritem.md) | Deprecated. Gets a specific item from a toolbar. |
| [IBrowserService2::_GetViewBorderRect](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_getviewborderrect.md) | Deprecated. Used with IBrowserService2 |
| [IBrowserService2::_Initialize](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_initialize.md) | Deprecated. Coordinates the initializing of state between the base and the derived classes. |
| [IBrowserService2::_LoadToolbars](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_loadtoolbars.md) | Deprecated. Loads the saved state of the browser's toolbars. |
| [IBrowserService2::_MaySaveChanges](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_maysavechanges.md) | Deprecated. Enables the base class to check whether the browser view needs to save changes before closing. |
| [IBrowserService2::_NavigateToPidl](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_navigatetopidl.md) | Deprecated. Navigates the base class to a new location synchronously. |
| [IBrowserService2::_OnFocusChange](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_onfocuschange.md) | Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view. |
| [IBrowserService2::_PauseOrResumeView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_pauseorresumeview.md) | Deprecated. Enables a derived class to request the base class to either pause (such as before a minimize operation) or resume the browser view. |
| [IBrowserService2::_ResizeNextBorderHelper](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_resizenextborderhelper.md) | Deprecated. A helper method used by the implementation of IBrowserService2 |
| [IBrowserService2::_ResizeNextBorder](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_resizenextborder.md) | Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars. |
| [IBrowserService2::_ResizeView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_resizeview.md) | Deprecated. Calls IBrowserService2 |
| [IBrowserService2::_SaveToolbars](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_savetoolbars.md) | Deprecated. Saves the state of browser toolbars. |
| [IBrowserService2::_SendChildren](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_sendchildren.md) | Deprecated. Allows the derived class to send a message through the SendMessage function directly instead of relying on the base class. |
| [IBrowserService2::_SetFocus](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_setfocus.md) | Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through TranslateAcceleratorSB or when IBrowserService2 |
| [IBrowserService2::_SwitchActivationNow](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_switchactivationnow.md) | Deprecated. Coordinates state updates while switching between current and pending browser views. |
| [IBrowserService2::_TryShell2Rename](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_tryshell2rename.md) | Deprecated. Coordinates the renaming of the current browser view when the browser is redirected. |
| [IBrowserService2::_UIActivateView](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_uiactivateview.md) | Deprecated. Allows a derived class to request that the base class update the browser view. |
| [IBrowserService2::_UpdateViewRectSize](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_updateviewrectsize.md) | Deprecated. Called to inform other functions involved in the browser view size negotiations that the allowable browser view dimensions have changed. |
| [IBrowserService2::_get_itbLastFocus](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_get_itblastfocus.md) | Deprecated. Gets the ID of the last toolbar or view that had focus. |
| [IBrowserService2::_put_itbLastFocus](..\shdeprecated\nf-shdeprecated-ibrowserservice2-_put_itblastfocus.md) | Deprecated. Sets the last toolbar or the last view with focus. |
| [IBrowserService2::v_CheckZoneCrossing](..\shdeprecated\nf-shdeprecated-ibrowserservice2-v_checkzonecrossing.md) | Deprecated. Called by the base class to validate a zone crossing when navigating from one page to another. |
| [IBrowserService2::v_GetViewStream](..\shdeprecated\nf-shdeprecated-ibrowserservice2-v_getviewstream.md) | Deprecated. Returns a stream used to load or save the view state. |
| [IBrowserService2::v_MayGetNextToolbarFocus](..\shdeprecated\nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus.md) | Deprecated. Used when translating accelerators through TranslateAcceleratorSB and in checking the cycle of focus between the view and the browser's toolbars. |
| [IBrowserService2::v_MayTranslateAccelerator](..\shdeprecated\nf-shdeprecated-ibrowserservice2-v_maytranslateaccelerator.md) | Deprecated. Called by a derived class to instruct the base class to proceed with the translation of keyboard mnemonics. |
| [IBrowserService2::v_ShowHideChildWindows](..\shdeprecated\nf-shdeprecated-ibrowserservice2-v_showhidechildwindows.md) | Deprecated. Allows a derived class to update its child windows after a sizing event. |
| [IBrowserService3::IEParseDisplayNameEx](..\shdeprecated\nf-shdeprecated-ibrowserservice3-ieparsedisplaynameex.md) | Deprecated. Parses a URL into a pointer to an item identifier list (PIDL). |
| [IBrowserService3::_PositionViewWindow](..\shdeprecated\nf-shdeprecated-ibrowserservice3-_positionviewwindow.md) | Deprecated. Used in view size negotiations. This method is called by _UpdateViewRectSize after determining the available dimensions. |
| [IBrowserService4::ActivateView](..\shdeprecated\nf-shdeprecated-ibrowserservice4-activateview.md) | Deprecated. |
| [IBrowserService4::SaveViewState](..\shdeprecated\nf-shdeprecated-ibrowserservice4-saveviewstate.md) | Deprecated. |
| [IBrowserService4::_ResizeAllBorders](..\shdeprecated\nf-shdeprecated-ibrowserservice4-_resizeallborders.md) | Deprecated. |
| [IBrowserService::CacheOLEServer](..\shdeprecated\nf-shdeprecated-ibrowserservice-cacheoleserver.md) | Deprecated. Caches a reference to an external object to avoid reloading the server on reuse. |
| [IBrowserService::CanNavigateNow](..\shdeprecated\nf-shdeprecated-ibrowserservice-cannavigatenow.md) | Deprecated. Returns a value that indicates whether navigation is currently allowed. |
| [IBrowserService::DisplayParseError](..\shdeprecated\nf-shdeprecated-ibrowserservice-displayparseerror.md) | Deprecated. Displays a URL that failed to be successfully parsed by IBrowserService |
| [IBrowserService::GetBrowserByIndex](..\shdeprecated\nf-shdeprecated-ibrowserservice-getbrowserbyindex.md) | Deprecated. Retrieves the browser with the given index. |
| [IBrowserService::GetBrowserIndex](..\shdeprecated\nf-shdeprecated-ibrowserservice-getbrowserindex.md) | Deprecated. Retrieves the index of the browser in the window hierarchy. |
| [IBrowserService::GetFlags](..\shdeprecated\nf-shdeprecated-ibrowserservice-getflags.md) | Deprecated. Retrieves the current set of browser flags. |
| [IBrowserService::GetHistoryObject](..\shdeprecated\nf-shdeprecated-ibrowserservice-gethistoryobject.md) | Deprecated. Retrieves an IOleObject that represents the browser's history object. |
| [IBrowserService::GetNavigateState](..\shdeprecated\nf-shdeprecated-ibrowserservice-getnavigatestate.md) | Deprecated. Retrieves the browser's current navigation state. |
| [IBrowserService::GetOleObject](..\shdeprecated\nf-shdeprecated-ibrowserservice-getoleobject.md) | Deprecated. Retrieves an IOleObject for the browser. |
| [IBrowserService::GetPalette](..\shdeprecated\nf-shdeprecated-ibrowserservice-getpalette.md) | Deprecated. Retrieves the browser's palette. |
| [IBrowserService::GetParentSite](..\shdeprecated\nf-shdeprecated-ibrowserservice-getparentsite.md) | Deprecated. Retrieves the browser parent's in-place client site. |
| [IBrowserService::GetPidl](..\shdeprecated\nf-shdeprecated-ibrowserservice-getpidl.md) | Deprecated. Retrieves a copy of the current pointer to an item identifier list (PIDL). |
| [IBrowserService::GetSetCodePage](..\shdeprecated\nf-shdeprecated-ibrowserservice-getsetcodepage.md) | Deprecated. Sets a new character code page and retrieves a pointer to the previous code page. |
| [IBrowserService::GetTitle](..\shdeprecated\nf-shdeprecated-ibrowserservice-gettitle.md) | Deprecated. Retrieves the title of a browser window. |
| [IBrowserService::GetTravelLog](..\shdeprecated\nf-shdeprecated-ibrowserservice-gettravellog.md) | Deprecated. Retrieves the browser's ITravelLog. |
| [IBrowserService::IEGetDisplayName](..\shdeprecated\nf-shdeprecated-ibrowserservice-iegetdisplayname.md) | Deprecated. Retrieves the URL that corresponds to a pointer to an item identifier list (PIDL). |
| [IBrowserService::IEParseDisplayName](..\shdeprecated\nf-shdeprecated-ibrowserservice-ieparsedisplayname.md) | Deprecated. Parses a URL into a pointer to an item identifier list (PIDL). |
| [IBrowserService::IsControlWindowShown](..\shdeprecated\nf-shdeprecated-ibrowserservice-iscontrolwindowshown.md) | Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible. |
| [IBrowserService::NavigateToPidl](..\shdeprecated\nf-shdeprecated-ibrowserservice-navigatetopidl.md) | Deprecated. Navigates the browser to the location indicated by a pointer to an item identifier list (PIDL). |
| [IBrowserService::NotifyRedirect](..\shdeprecated\nf-shdeprecated-ibrowserservice-notifyredirect.md) | Deprecated. Updates the browser to the specified pointer to an item identifier list (PIDL), navigating if necessary. This method is called when a page is redirected. |
| [IBrowserService::OnHttpEquiv](..\shdeprecated\nf-shdeprecated-ibrowserservice-onhttpequiv.md) | Deprecated. Called when the document object responds to an HTTP-EQUIV metatag by issuing either the OLECMDID_HTTPEQUIV or OLECMDID_HTTPEQUIV_DONE command through IOleCommandTarget |
| [IBrowserService::RegisterWindow](..\shdeprecated\nf-shdeprecated-ibrowserservice-registerwindow.md) | Deprecated. Registers the browser in the list of browser windows. |
| [IBrowserService::SetFlags](..\shdeprecated\nf-shdeprecated-ibrowserservice-setflags.md) | Deprecated. Sets flags that indicate browser status. |
| [IBrowserService::SetHistoryObject](..\shdeprecated\nf-shdeprecated-ibrowserservice-sethistoryobject.md) | Deprecated. Sets the browser's history object. |
| [IBrowserService::SetNavigateState](..\shdeprecated\nf-shdeprecated-ibrowserservice-setnavigatestate.md) | Deprecated. Sets the current navigation state. This method affects the cursor and animation. |
| [IBrowserService::SetReferrer](..\shdeprecated\nf-shdeprecated-ibrowserservice-setreferrer.md) | Deprecated. Sets the pointer to an item identifier list (PIDL) used for zone checking when creating a new window. |
| [IBrowserService::SetTitle](..\shdeprecated\nf-shdeprecated-ibrowserservice-settitle.md) | Deprecated. Sets the title of a browser window. |
| [IBrowserService::ShowControlWindow](..\shdeprecated\nf-shdeprecated-ibrowserservice-showcontrolwindow.md) | Deprecated. Shows or hides various frame controls. |
| [IBrowserService::UpdateBackForwardState](..\shdeprecated\nf-shdeprecated-ibrowserservice-updatebackforwardstate.md) | Deprecated. Updates the state of the browser's Back and Forward buttons. |
| [IBrowserService::UpdateWindowList](..\shdeprecated\nf-shdeprecated-ibrowserservice-updatewindowlist.md) | Deprecated. Instructs the browser to update the pointer to an item identifier list (PIDL) in the window list. This method is called after navigation. |
| [IConnectableCredentialProviderCredential::Connect](..\credentialprovider\nf-credentialprovider-iconnectablecredentialprovidercredential-connect.md) | Connects an IConnectableCredentialProviderCredential object. This method is called after the user clicks the Submit button within the Pre-Logon-Access Provider screen and before ICredentialProviderCredential |
| [IConnectableCredentialProviderCredential::Disconnect](..\credentialprovider\nf-credentialprovider-iconnectablecredentialprovidercredential-disconnect.md) | Disconnects an IConnectableCredentialProviderCredential object. |
| [ICredentialProvider::Advise](..\credentialprovider\nf-credentialprovider-icredentialprovider-advise.md) | Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface. |
| [ICredentialProvider::GetCredentialAt](..\credentialprovider\nf-credentialprovider-icredentialprovider-getcredentialat.md) | Gets a specific credential. |
| [ICredentialProvider::GetCredentialCount](..\credentialprovider\nf-credentialprovider-icredentialprovider-getcredentialcount.md) | Gets the number of available credentials under this credential provider. |
| [ICredentialProvider::GetFieldDescriptorAt](..\credentialprovider\nf-credentialprovider-icredentialprovider-getfielddescriptorat.md) | Gets metadata that describes a specified field. |
| [ICredentialProvider::GetFieldDescriptorCount](..\credentialprovider\nf-credentialprovider-icredentialprovider-getfielddescriptorcount.md) | Retrieves the count of fields in the needed to display this provider's credentials. |
| [ICredentialProvider::SetSerialization](..\credentialprovider\nf-credentialprovider-icredentialprovider-setserialization.md) | Sets the serialization characteristics of the credential provider. |
| [ICredentialProvider::SetUsageScenario](..\credentialprovider\nf-credentialprovider-icredentialprovider-setusagescenario.md) | Defines the scenarios for which the credential provider is valid. Called whenever the credential provider is initialized. |
| [ICredentialProvider::UnAdvise](..\credentialprovider\nf-credentialprovider-icredentialprovider-unadvise.md) | Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted. |
| [ICredentialProviderCredential2::GetUserSid](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential2-getusersid.md) | Retrieves the security identifier (SID) of the user that is associated with this credential. |
| [ICredentialProviderCredential::Advise](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-advise.md) | Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in ICredentialProviderCredential interface. |
| [ICredentialProviderCredential::CommandLinkClicked](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-commandlinkclicked.md) | Enables the Logon UI and Credential UI to indicate that a link was clicked. |
| [ICredentialProviderCredential::GetBitmapValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getbitmapvalue.md) | Enables retrieval of bitmap data from a credential with a bitmap field. |
| [ICredentialProviderCredential::GetCheckboxValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getcheckboxvalue.md) | Retrieves the checkbox value. |
| [ICredentialProviderCredential::GetComboBoxValueAt](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getcomboboxvalueat.md) | Gets the string label for a combo box entry at the given index. |
| [ICredentialProviderCredential::GetComboBoxValueCount](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getcomboboxvaluecount.md) | Gets a count of the items in the specified combo box and designates which item should have initial selection. |
| [ICredentialProviderCredential::GetFieldState](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getfieldstate.md) | Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile. |
| [ICredentialProviderCredential::GetSerialization](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getserialization.md) | Called in response to an attempt to submit this credential to the underlying authentication engine. |
| [ICredentialProviderCredential::GetStringValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getstringvalue.md) | Enables retrieval of text from a credential with a text field. |
| [ICredentialProviderCredential::GetSubmitButtonValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-getsubmitbuttonvalue.md) | Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI. |
| [ICredentialProviderCredential::ReportResult](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-reportresult.md) | Translates a received error status code into the appropriate user-readable message. |
| [ICredentialProviderCredential::SetCheckboxValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-setcheckboxvalue.md) | Enables a Logon UI and Credential UI to indicate that a checkbox value has changed. |
| [ICredentialProviderCredential::SetComboBoxSelectedValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-setcomboboxselectedvalue.md) | Enables a Logon UI and Credential UI to indicate that a combo box value has been selected. |
| [ICredentialProviderCredential::SetDeselected](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-setdeselected.md) | Called when a credential loses selection. |
| [ICredentialProviderCredential::SetSelected](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-setselected.md) | Called when a credential is selected. Enables the implementer to set logon characteristics. |
| [ICredentialProviderCredential::SetStringValue](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-setstringvalue.md) | Enables a Logon UI or Credential UI to update the text for a CPFT_EDIT_TEXT fields as the user types in them. |
| [ICredentialProviderCredential::UnAdvise](..\credentialprovider\nf-credentialprovider-icredentialprovidercredential-unadvise.md) | Used by the Logon UI or Credential UI to advise the credential that event callbacks are no longer accepted. |
| [ICredentialProviderCredentialEvents2::BeginFieldUpdates](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates.md) | Starts a batch update to fields in the logon or credential UI. |
| [ICredentialProviderCredentialEvents2::EndFieldUpdates](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents2-endfieldupdates.md) | Finishes and commits the batch updates started by BeginFieldUpdates. |
| [ICredentialProviderCredentialEvents2::SetFieldOptions](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions.md) | Specifies whether a specified field in the logon or credential UI should display a &#0034;password reveal&#0034; glyph or is expected to receive an e-mail address. |
| [ICredentialProviderCredentialEvents::AppendFieldComboBoxItem](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-appendfieldcomboboxitem.md) | Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-deletefieldcomboboxitem.md) | Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::OnCreatingWindow](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-oncreatingwindow.md) | Called when the window is created. Enables credentials to retrieve the HWND of the parent window after Advise is called. |
| [ICredentialProviderCredentialEvents::SetFieldBitmap](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldbitmap.md) | Communicates to the Logon UI or Credential UI that a tile image field has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldCheckbox](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldcheckbox.md) | Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldcomboboxselecteditem.md) | Communicates to the Logon UI or Credential UI that the selected item in a combo box has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldInteractiveState](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldinteractivestate.md) | Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldState](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldstate.md) | Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldString](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldstring.md) | Communicates to the Logon UI or Credential UI that the string associated with a field has changed and that the UI should be updated. |
| [ICredentialProviderCredentialEvents::SetFieldSubmitButton](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialevents-setfieldsubmitbutton.md) | Enables credentials to set the field that the submit button appears adjacent to. |
| [ICredentialProviderCredentialWithFieldOptions::GetFieldOptions](..\credentialprovider\nf-credentialprovider-icredentialprovidercredentialwithfieldoptions-getfieldoptions.md) | Retrieves the current option set for a specified field in a logon or credential UI. Called by the credential provider framework. |
| [ICredentialProviderEvents::CredentialsChanged](..\credentialprovider\nf-credentialprovider-icredentialproviderevents-credentialschanged.md) | Signals the Logon UI or Credential UI that the enumerated list of credentials has changed. |
| [ICredentialProviderFilter::Filter](..\credentialprovider\nf-credentialprovider-icredentialproviderfilter-filter.md) | Evaluates whether a list of credential providers should be allowed to provide credential tiles. |
| [ICredentialProviderFilter::UpdateRemoteCredential](..\credentialprovider\nf-credentialprovider-icredentialproviderfilter-updateremotecredential.md) | Updates a credential from a remote session. |
| [ICredentialProviderSetUserArray::SetUserArray](..\credentialprovider\nf-credentialprovider-icredentialprovidersetuserarray-setuserarray.md) | Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI. |
| [ICredentialProviderUser::GetProviderID](..\credentialprovider\nf-credentialprovider-icredentialprovideruser-getproviderid.md) | Retrieves the ID of the account provider for this user. |
| [ICredentialProviderUser::GetSid](..\credentialprovider\nf-credentialprovider-icredentialprovideruser-getsid.md) | Retrieves the user's security identifier (SID). |
| [ICredentialProviderUser::GetStringValue](..\credentialprovider\nf-credentialprovider-icredentialprovideruser-getstringvalue.md) | Retrieves string properties from the ICredentialProviderUser object based on the input value. |
| [ICredentialProviderUser::GetValue](..\credentialprovider\nf-credentialprovider-icredentialprovideruser-getvalue.md) | Retrieves a specified property value set for the user. |
| [ICredentialProviderUserArray::GetAccountOptions](..\credentialprovider\nf-credentialprovider-icredentialprovideruserarray-getaccountoptions.md) | Retrieves a value that indicates whether the &#0034;Other user&#0034; tile for local or Microsoft accounts is shown in the logon or credential UI. |
| [ICredentialProviderUserArray::GetAt](..\credentialprovider\nf-credentialprovider-icredentialprovideruserarray-getat.md) | Retrieves a specified user from the array. |
| [ICredentialProviderUserArray::GetCount](..\credentialprovider\nf-credentialprovider-icredentialprovideruserarray-getcount.md) | Retrieves the number of ICredentialProviderUser objects in the user array. |
| [ICredentialProviderUserArray::SetProviderFilter](..\credentialprovider\nf-credentialprovider-icredentialprovideruserarray-setproviderfilter.md) | Limits the set of users in the array to either local accounts or Microsoft accounts. |
| [IEnumPublishedApps::Next](..\shappmgr\nf-shappmgr-ienumpublishedapps-next.md) | Gets the next IPublishedApp object in the enumeration. |
| [IEnumPublishedApps::Reset](..\shappmgr\nf-shappmgr-ienumpublishedapps-reset.md) | Resets the enumeration of IPublishedApp objects to the first item. |
| [IEnumSyncMgrConflict::Clone](..\syncmgr\nf-syncmgr-ienumsyncmgrconflict-clone.md) | Not used. Clones an IEnumSyncMgrConflict object. |
| [IEnumSyncMgrConflict::Next](..\syncmgr\nf-syncmgr-ienumsyncmgrconflict-next.md) | Gets the next batch of conflicts from the conflicts store. |
| [IEnumSyncMgrConflict::Reset](..\syncmgr\nf-syncmgr-ienumsyncmgrconflict-reset.md) | Resets the current position in the enumeration to zero. |
| [IEnumSyncMgrConflict::Skip](..\syncmgr\nf-syncmgr-ienumsyncmgrconflict-skip.md) | Skips forward the specified number of conflicts in the enumeration. |
| [IEnumSyncMgrEvents::Clone](..\syncmgr\nf-syncmgr-ienumsyncmgrevents-clone.md) | Clones an IEnumSyncMgrEvents object. |
| [IEnumSyncMgrEvents::Next](..\syncmgr\nf-syncmgr-ienumsyncmgrevents-next.md) | Gets the next batch of events from the event store. |
| [IEnumSyncMgrEvents::Reset](..\syncmgr\nf-syncmgr-ienumsyncmgrevents-reset.md) | Resets the current location in the enumeration to zero. |
| [IEnumSyncMgrEvents::Skip](..\syncmgr\nf-syncmgr-ienumsyncmgrevents-skip.md) | Skips forward the specified number of events in the enumeration. |
| [IEnumSyncMgrSyncItems::Clone](..\syncmgr\nf-syncmgr-ienumsyncmgrsyncitems-clone.md) | Not used. Clones an IEnumSyncMgrSyncItems object. |
| [IEnumSyncMgrSyncItems::Next](..\syncmgr\nf-syncmgr-ienumsyncmgrsyncitems-next.md) | Gets the next batch of sync items from the handler. |
| [IEnumSyncMgrSyncItems::Reset](..\syncmgr\nf-syncmgr-ienumsyncmgrsyncitems-reset.md) | Resets the current position in the enumeration to 0. |
| [IEnumSyncMgrSyncItems::Skip](..\syncmgr\nf-syncmgr-ienumsyncmgrsyncitems-skip.md) | Skips forward in the enumeration the specified number of items. |
| [IExpDispSupport::OnInvoke](..\shdeprecated\nf-shdeprecated-iexpdispsupport-oninvoke.md) | Deprecated. Gets ambient properties. |
| [IExpDispSupport::OnTranslateAccelerator](..\shdeprecated\nf-shdeprecated-iexpdispsupport-ontranslateaccelerator.md) | Deprecated. Instructs the control site to process the keystroke described in pMsg and modified by the flags in grfModifiers. |
| [IExpDispSupportXP::FindCIE4ConnectionPoint](..\shdeprecated\nf-shdeprecated-iexpdispsupportxp-findcie4connectionpoint.md) | Deprecated. Gets a connection point for browser events. |
| [IInputPanelConfiguration::EnableFocusTracking](..\inputpanelconfiguration\nf-inputpanelconfiguration-iinputpanelconfiguration-enablefocustracking.md) | Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps that controls the invoking and dismissing semantics of the touch keyboard. |
| [IInputPanelInvocationConfiguration::RequireTouchInEditControl](..\inputpanelconfiguration\nf-inputpanelconfiguration-iinputpanelinvocationconfiguration-requiretouchineditcontrol.md) | Requires an explicit user tap in an edit field before the touch keyboard invokes. |
| [IObjectArray::GetAt](..\objectarray\nf-objectarray-iobjectarray-getat.md) | Provides a pointer to a specified object's interface. The object and interface are specified by index and interface ID. |
| [IObjectArray::GetCount](..\objectarray\nf-objectarray-iobjectarray-getcount.md) | Provides a count of the objects in the collection. |
| [IObjectCollection::AddFromArray](..\objectarray\nf-objectarray-iobjectcollection-addfromarray.md) | Adds the objects contained in an IObjectArray to the collection. |
| [IObjectCollection::AddObject](..\objectarray\nf-objectarray-iobjectcollection-addobject.md) | Adds a single object to the collection. |
| [IObjectCollection::Clear](..\objectarray\nf-objectarray-iobjectcollection-clear.md) | Removes all objects from the collection. |
| [IObjectCollection::RemoveObjectAt](..\objectarray\nf-objectarray-iobjectcollection-removeobjectat.md) | Removes a single, specified object from the collection. |
| [IPublishedApp2::Install2](..\shappmgr\nf-shappmgr-ipublishedapp2-install2.md) | Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread. |
| [IPublishedApp::GetPublishedAppInfo](..\shappmgr\nf-shappmgr-ipublishedapp-getpublishedappinfo.md) | Gets publishing-related information about an application published by an application publisher. |
| [IPublishedApp::Install](..\shappmgr\nf-shappmgr-ipublishedapp-install.md) | Installs an application published by an application publisher. This method is invoked when the user selects Add or Add Later in Add/Remove Programs in Control Panel. |
| [IPublishedApp::Unschedule](..\shappmgr\nf-shappmgr-ipublishedapp-unschedule.md) | Cancels the installation of an application published by an application publisher. |
| [IQueryContinueWithStatus::SetStatusMessage](..\credentialprovider\nf-credentialprovider-iquerycontinuewithstatus-setstatusmessage.md) | Enables the credential provider to set status messages as it attempts to complete IConnectableCredentialProviderCredential |
| [ISharedBitmap::Detach](..\thumbcache\nf-thumbcache-isharedbitmap-detach.md) | Retrieves the bitmap contained in an ISharedBitmap object, and returns a copy if the contained bitmap resides in shared memory. |
| [ISharedBitmap::GetFormat](..\thumbcache\nf-thumbcache-isharedbitmap-getformat.md) | Retrieves the alpha type of the bitmap image. |
| [ISharedBitmap::GetSharedBitmap](..\thumbcache\nf-thumbcache-isharedbitmap-getsharedbitmap.md) | Retrieves the bitmap contained in an ISharedBitmap object. |
| [ISharedBitmap::GetSize](..\thumbcache\nf-thumbcache-isharedbitmap-getsize.md) | Retrieves the size of the bitmap contained in an ISharedBitmap object. |
| [ISharedBitmap::InitializeBitmap](..\thumbcache\nf-thumbcache-isharedbitmap-initializebitmap.md) | Initializes a new ISharedBitmap object with a given bitmap. |
| [IShellApp::GetAppInfo](..\shappmgr\nf-shappmgr-ishellapp-getappinfo.md) | Gets general information about an application. |
| [IShellApp::GetCachedSlowAppInfo](..\shappmgr\nf-shappmgr-ishellapp-getcachedslowappinfo.md) | Returns information to the application that originates from a slow source. Unlike IShellApp |
| [IShellApp::GetPossibleActions](..\shappmgr\nf-shappmgr-ishellapp-getpossibleactions.md) | Gets a bitmask of management actions allowed for an application. |
| [IShellApp::GetSlowAppInfo](..\shappmgr\nf-shappmgr-ishellapp-getslowappinfo.md) | Returns information to the application that originates from a slow source. This method is not applicable to published applications. |
| [IShellApp::IsInstalled](..\shappmgr\nf-shappmgr-ishellapp-isinstalled.md) | Gets a value indicating whether a specified application is currently installed. |
| [IShellImageData::CloneFrame](..\shimgdata\nf-shimgdata-ishellimagedata-cloneframe.md) | Retrieves a clone of the current image or frame. |
| [IShellImageData::Decode](..\shimgdata\nf-shimgdata-ishellimagedata-decode.md) | Decodes the image file, setting state. |
| [IShellImageData::DiscardEdit](..\shimgdata\nf-shimgdata-ishellimagedata-discardedit.md) | Discards edits made to an image. |
| [IShellImageData::DisplayName](..\shimgdata\nf-shimgdata-ishellimagedata-displayname.md) | Gets the name of the file if IShellImageData was initialized on a file path. Otherwise, gets the name of the data stream. |
| [IShellImageData::Draw](..\shimgdata\nf-shimgdata-ishellimagedata-draw.md) | Draws a decoded image. |
| [IShellImageData::GetCurrentPage](..\shimgdata\nf-shimgdata-ishellimagedata-getcurrentpage.md) | Gets the current page of a multipage image. |
| [IShellImageData::GetDelay](..\shimgdata\nf-shimgdata-ishellimagedata-getdelay.md) | Gets the delay value for the current frame of an animation. |
| [IShellImageData::GetEncoderParams](..\shimgdata\nf-shimgdata-ishellimagedata-getencoderparams.md) | Gets the current set of encoder parameters. |
| [IShellImageData::GetPageCount](..\shimgdata\nf-shimgdata-ishellimagedata-getpagecount.md) | Gets the number of pages in a multipage image. |
| [IShellImageData::GetPixelFormat](..\shimgdata\nf-shimgdata-ishellimagedata-getpixelformat.md) | Gets the pixel format of the image. |
| [IShellImageData::GetProperties](..\shimgdata\nf-shimgdata-ishellimagedata-getproperties.md) | Gets an IPropertySetStorage through which the properties of the image can be accessed. |
| [IShellImageData::GetRawDataFormat](..\shimgdata\nf-shimgdata-ishellimagedata-getrawdataformat.md) | Retrieves a GUID that identifies the format of the image. |
| [IShellImageData::GetResolution](..\shimgdata\nf-shimgdata-ishellimagedata-getresolution.md) | Gets the resolution, in dots per inch (dpi), of the image. |
| [IShellImageData::GetSize](..\shimgdata\nf-shimgdata-ishellimagedata-getsize.md) | Gets the dimensions of the image file. |
| [IShellImageData::IsAnimated](..\shimgdata\nf-shimgdata-ishellimagedata-isanimated.md) | Determines whether the image is animated. |
| [IShellImageData::IsDecoded](..\shimgdata\nf-shimgdata-ishellimagedata-isdecoded.md) | Determines whether the image has been decoded by calling IShellImageData |
| [IShellImageData::IsEditable](..\shimgdata\nf-shimgdata-ishellimagedata-iseditable.md) | Determines whether the image can be edited. |
| [IShellImageData::IsMultipage](..\shimgdata\nf-shimgdata-ishellimagedata-ismultipage.md) | Determines whether the image is a multipage Tagged Image File Format (TIFF) image. |
| [IShellImageData::IsPrintable](..\shimgdata\nf-shimgdata-ishellimagedata-isprintable.md) | Determines whether the image can be printed. |
| [IShellImageData::IsTransparent](..\shimgdata\nf-shimgdata-ishellimagedata-istransparent.md) | Determines whether the image is transparent. |
| [IShellImageData::IsVector](..\shimgdata\nf-shimgdata-ishellimagedata-isvector.md) | Determines whether the image is a vector image. |
| [IShellImageData::NextFrame](..\shimgdata\nf-shimgdata-ishellimagedata-nextframe.md) | Switches to the next frame of an animated image. |
| [IShellImageData::NextPage](..\shimgdata\nf-shimgdata-ishellimagedata-nextpage.md) | Switches to the next page of a multipage image. Any associated animations are reset. |
| [IShellImageData::PrevPage](..\shimgdata\nf-shimgdata-ishellimagedata-prevpage.md) | Switches to the previous page of a multipage image. Any associated animations are reset. |
| [IShellImageData::RegisterAbort](..\shimgdata\nf-shimgdata-ishellimagedata-registerabort.md) | Sets a callback abort object, optionally returning a pointer to the previous object. |
| [IShellImageData::ReplaceFrame](..\shimgdata\nf-shimgdata-ishellimagedata-replaceframe.md) | Replaces the current frame with a new image. |
| [IShellImageData::Rotate](..\shimgdata\nf-shimgdata-ishellimagedata-rotate.md) | Rotates an image in increments of 90 degrees. |
| [IShellImageData::Scale](..\shimgdata\nf-shimgdata-ishellimagedata-scale.md) | Adjusts the size of an image. |
| [IShellImageData::SelectPage](..\shimgdata\nf-shimgdata-ishellimagedata-selectpage.md) | Selects a specified page in a multipage image. |
| [IShellImageData::SetEncoderParams](..\shimgdata\nf-shimgdata-ishellimagedata-setencoderparams.md) | Sets encoder parameters. |
| [IShellImageDataAbort::QueryAbort](..\shimgdata\nf-shimgdata-ishellimagedataabort-queryabort.md) | Aborts an IShellImageData process such as Decode, Draw, or Scale. This is a callback method. |
| [IShellImageDataFactory::CreateIShellImageData](..\shimgdata\nf-shimgdata-ishellimagedatafactory-createishellimagedata.md) | Creates an instance of the IShellImageData interface. |
| [IShellImageDataFactory::CreateImageFromFile](..\shimgdata\nf-shimgdata-ishellimagedatafactory-createimagefromfile.md) | Creates an instance of the IShellImageData interface based on a given file. |
| [IShellImageDataFactory::CreateImageFromStream](..\shimgdata\nf-shimgdata-ishellimagedatafactory-createimagefromstream.md) | Creates an instance of the IShellImageData interface based on a given file stream. |
| [IShellImageDataFactory::GetDataFormatFromPath](..\shimgdata\nf-shimgdata-ishellimagedatafactory-getdataformatfrompath.md) | Determines a file's format based on its extension. |
| [IShellService::SetOwner](..\shdeprecated\nf-shdeprecated-ishellservice-setowner.md) | Deprecated. Declares an owner reference to the service object. |
| [IStorageProviderHandler::GetPropertyHandlerFromFileId](..\storageprovider\nf-storageprovider-istorageproviderhandler-getpropertyhandlerfromfileid.md) | Gets an instance of IStorageProviderPropertyHandler associated with the provided file identifier. |
| [IStorageProviderHandler::GetPropertyHandlerFromPath](..\storageprovider\nf-storageprovider-istorageproviderhandler-getpropertyhandlerfrompath.md) | Gets an instance of IStorageProviderPropertyHandler associated with the provided path. |
| [IStorageProviderHandler::GetPropertyHandlerFromUri](..\storageprovider\nf-storageprovider-istorageproviderhandler-getpropertyhandlerfromuri.md) | Gets an instance of IStorageProviderPropertyHandler associated with the provided URI. |
| [IStorageProviderPropertyHandler::RetrieveProperties](..\storageprovider\nf-storageprovider-istorageproviderpropertyhandler-retrieveproperties.md) | Gets the properties managed by the sync engine. |
| [ISyncMgrConflict::GetConflictIdInfo](..\syncmgr\nf-syncmgr-isyncmgrconflict-getconflictidinfo.md) | Gets information that identifies a conflict within a conflict store. |
| [ISyncMgrConflict::GetItemsArray](..\syncmgr\nf-syncmgr-isyncmgrconflict-getitemsarray.md) | Retrieves a conflict items array. |
| [ISyncMgrConflict::GetProperty](..\syncmgr\nf-syncmgr-isyncmgrconflict-getproperty.md) | Gets a conflict property, given a property key. |
| [ISyncMgrConflict::GetResolutionHandler](..\syncmgr\nf-syncmgr-isyncmgrconflict-getresolutionhandler.md) | Gets the resolution handler for the conflict. |
| [ISyncMgrConflict::Resolve](..\syncmgr\nf-syncmgr-isyncmgrconflict-resolve.md) | Resolves the conflict using its own sync handler, controls UI. |
| [ISyncMgrConflictFolder::GetConflictIDList](..\syncmgr\nf-syncmgr-isyncmgrconflictfolder-getconflictidlist.md) | Maps a conflict to its IShellItem. |
| [ISyncMgrConflictItems::GetCount](..\syncmgr\nf-syncmgr-isyncmgrconflictitems-getcount.md) | Gets the conflict item count. |
| [ISyncMgrConflictItems::GetItem](..\syncmgr\nf-syncmgr-isyncmgrconflictitems-getitem.md) | Gets a specified conflict data item. |
| [ISyncMgrConflictPresenter::PresentConflict](..\syncmgr\nf-syncmgr-isyncmgrconflictpresenter-presentconflict.md) | Presents the conflict to the user. |
| [ISyncMgrConflictResolutionItems::GetCount](..\syncmgr\nf-syncmgr-isyncmgrconflictresolutionitems-getcount.md) | Gets item count. |
| [ISyncMgrConflictResolutionItems::GetItem](..\syncmgr\nf-syncmgr-isyncmgrconflictresolutionitems-getitem.md) | Gets result information for a specified item, when successful. |
| [ISyncMgrConflictResolveInfo::GetItemChoiceCount](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoicecount.md) | Gets the number of items that the user wants to keep. |
| [ISyncMgrConflictResolveInfo::GetItemChoice](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoice.md) | Gets the index of an item that the user wants to keep. |
| [ISyncMgrConflictResolveInfo::GetIterationInfo](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-getiterationinfo.md) | Gets information about which conflict in a set of conflicts is being resolved. |
| [ISyncMgrConflictResolveInfo::GetPresenterChoice](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-getpresenterchoice.md) | Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set. |
| [ISyncMgrConflictResolveInfo::GetPresenterNextStep](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-getpresenternextstep.md) | Gets what the presenter wants to do as the next step in the sync manager conflict resolution. |
| [ISyncMgrConflictResolveInfo::SetItemChoices](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-setitemchoices.md) | Sets the array of indexes that represents which items the user wants to keep. This method is used when the user chooses to apply the same operation to all selected conflicts of the same type from the same handler. |
| [ISyncMgrConflictResolveInfo::SetPresenterChoice](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-setpresenterchoice.md) | Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set. |
| [ISyncMgrConflictResolveInfo::SetPresenterNextStep](..\syncmgr\nf-syncmgr-isyncmgrconflictresolveinfo-setpresenternextstep.md) | Sets what the presenter wants to do as the next step in the sync manager conflict resolution. |
| [ISyncMgrConflictStore::BindToConflict](..\syncmgr\nf-syncmgr-isyncmgrconflictstore-bindtoconflict.md) | Binds to a particular conflict specified by IID. |
| [ISyncMgrConflictStore::EnumConflicts](..\syncmgr\nf-syncmgr-isyncmgrconflictstore-enumconflicts.md) | Enumerates conflicts scoped to the provided sync handler and sync item. |
| [ISyncMgrConflictStore::GetCount](..\syncmgr\nf-syncmgr-isyncmgrconflictstore-getcount.md) | Gets the number of conflicts in the store. |
| [ISyncMgrConflictStore::RemoveConflicts](..\syncmgr\nf-syncmgr-isyncmgrconflictstore-removeconflicts.md) | Deletes a set of conflicts, specified by conflict ID, from the store. |
| [ISyncMgrControl::ActivateHandler](..\syncmgr\nf-syncmgr-isyncmgrcontrol-activatehandler.md) | Activates or deactivates a handler. |
| [ISyncMgrControl::EnableHandler](..\syncmgr\nf-syncmgr-isyncmgrcontrol-enablehandler.md) | Enables or disables a handler. |
| [ISyncMgrControl::EnableItem](..\syncmgr\nf-syncmgr-isyncmgrcontrol-enableitem.md) | Enables or disables a sync item managed by a specified handler. |
| [ISyncMgrControl::StartHandlerSync](..\syncmgr\nf-syncmgr-isyncmgrcontrol-starthandlersync.md) | Initiates the synchronization of all items managed by a particular handler. |
| [ISyncMgrControl::StartItemSync](..\syncmgr\nf-syncmgr-isyncmgrcontrol-startitemsync.md) | Initiates the synchronization of specified items managed by a particular handler. |
| [ISyncMgrControl::StartSyncAll](..\syncmgr\nf-syncmgr-isyncmgrcontrol-startsyncall.md) | Synchronizes all items managed by all handlers. |
| [ISyncMgrControl::StopHandlerSync](..\syncmgr\nf-syncmgr-isyncmgrcontrol-stophandlersync.md) | Stops the synchronization of a specified handler. |
| [ISyncMgrControl::StopItemSync](..\syncmgr\nf-syncmgr-isyncmgrcontrol-stopitemsync.md) | Stops the synchronization of specified items managed by a particular handler. |
| [ISyncMgrControl::StopSyncAll](..\syncmgr\nf-syncmgr-isyncmgrcontrol-stopsyncall.md) | Stops the synchronization of all items managed by all handlers. |
| [ISyncMgrControl::UpdateConflicts](..\syncmgr\nf-syncmgr-isyncmgrcontrol-updateconflicts.md) | Informs Sync Center that conflicts have been added for a specific handler or item. |
| [ISyncMgrControl::UpdateEvents](..\syncmgr\nf-syncmgr-isyncmgrcontrol-updateevents.md) | Informs Sync Center that events have been added for a specific handler or item. |
| [ISyncMgrControl::UpdateHandlerCollection](..\syncmgr\nf-syncmgr-isyncmgrcontrol-updatehandlercollection.md) | Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed. |
| [ISyncMgrControl::UpdateHandler](..\syncmgr\nf-syncmgr-isyncmgrcontrol-updatehandler.md) | Instructs Sync Center to reenumerate the items managed by a handler or informs it that properties of the handler have changed. |
| [ISyncMgrControl::UpdateItem](..\syncmgr\nf-syncmgr-isyncmgrcontrol-updateitem.md) | Informs Sync Center that properties of a sync item have changed. |
| [ISyncMgrEnumItems::Clone](..\mobsync\nf-mobsync-isyncmgrenumitems-clone.md) | Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. |
| [ISyncMgrEnumItems::Next](..\mobsync\nf-mobsync-isyncmgrenumitems-next.md) | Enumerates the next celt elements in the enumerator's list, returning them in rgelt along with the actual number of enumerated elements in pceltFetched. |
| [ISyncMgrEnumItems::Reset](..\mobsync\nf-mobsync-isyncmgrenumitems-reset.md) | Instructs the enumerator to position itself at the beginning of the list of elements. |
| [ISyncMgrEnumItems::Skip](..\mobsync\nf-mobsync-isyncmgrenumitems-skip.md) | Instructs the enumerator to skip the next celt elements in the enumeration so that the next call to ISyncMgrEnumItems |
| [ISyncMgrEvent::GetContext](..\syncmgr\nf-syncmgr-isyncmgrevent-getcontext.md) | Gets a context object that can be used by a handler to display properties or execute a context menu action. |
| [ISyncMgrEvent::GetDescription](..\syncmgr\nf-syncmgr-isyncmgrevent-getdescription.md) | Gets the event description. |
| [ISyncMgrEvent::GetEventID](..\syncmgr\nf-syncmgr-isyncmgrevent-geteventid.md) | Gets the event ID. |
| [ISyncMgrEvent::GetFlags](..\syncmgr\nf-syncmgr-isyncmgrevent-getflags.md) | Gets event flags. |
| [ISyncMgrEvent::GetHandlerID](..\syncmgr\nf-syncmgr-isyncmgrevent-gethandlerid.md) | Gets the ID of the handler for which the event was logged. |
| [ISyncMgrEvent::GetItemID](..\syncmgr\nf-syncmgr-isyncmgrevent-getitemid.md) | Gets the ID of the item for which the event was logged. |
| [ISyncMgrEvent::GetLevel](..\syncmgr\nf-syncmgr-isyncmgrevent-getlevel.md) | Gets the log level of the event. |
| [ISyncMgrEvent::GetLinkReference](..\syncmgr\nf-syncmgr-isyncmgrevent-getlinkreference.md) | Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder. |
| [ISyncMgrEvent::GetLinkText](..\syncmgr\nf-syncmgr-isyncmgrevent-getlinktext.md) | Gets the text for the hot link for the event. |
| [ISyncMgrEvent::GetName](..\syncmgr\nf-syncmgr-isyncmgrevent-getname.md) | Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event. |
| [ISyncMgrEvent::GetTime](..\syncmgr\nf-syncmgr-isyncmgrevent-gettime.md) | Gets the creation time. |
| [ISyncMgrEventLinkUIOperation::Init](..\syncmgr\nf-syncmgr-isyncmgreventlinkuioperation-init.md) | Enables Sync Center to provide the event to link to so ISyncMgrUIOperation |
| [ISyncMgrEventStore::GetEventCount](..\syncmgr\nf-syncmgr-isyncmgreventstore-geteventcount.md) | Gets the event count. |
| [ISyncMgrEventStore::GetEventEnumerator](..\syncmgr\nf-syncmgr-isyncmgreventstore-geteventenumerator.md) | Gets an enumerator for a handler's events. |
| [ISyncMgrEventStore::GetEvent](..\syncmgr\nf-syncmgr-isyncmgreventstore-getevent.md) | Gets a specified event object. |
| [ISyncMgrEventStore::RemoveEvent](..\syncmgr\nf-syncmgr-isyncmgreventstore-removeevent.md) | Removes events, as specified. |
| [ISyncMgrHandler::Activate](..\syncmgr\nf-syncmgr-isyncmgrhandler-activate.md) | Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot. |
| [ISyncMgrHandler::Enable](..\syncmgr\nf-syncmgr-isyncmgrhandler-enable.md) | Requests that an active handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot. |
| [ISyncMgrHandler::GetCapabilities](..\syncmgr\nf-syncmgr-isyncmgrhandler-getcapabilities.md) | Gets a set of flags describing the handler's defined capabilities. |
| [ISyncMgrHandler::GetHandlerInfo](..\syncmgr\nf-syncmgr-isyncmgrhandler-gethandlerinfo.md) | Gets properties that describe the handler. |
| [ISyncMgrHandler::GetName](..\syncmgr\nf-syncmgr-isyncmgrhandler-getname.md) | Gets the display name of the handler. |
| [ISyncMgrHandler::GetObject](..\syncmgr\nf-syncmgr-isyncmgrhandler-getobject.md) | Creates a specific type of object related to the handler. |
| [ISyncMgrHandler::GetPolicies](..\syncmgr\nf-syncmgr-isyncmgrhandler-getpolicies.md) | Gets a set of flags describing the policies set by the handler. |
| [ISyncMgrHandler::Synchronize](..\syncmgr\nf-syncmgr-isyncmgrhandler-synchronize.md) | Initiates a synchronization of a selection of the handler's sync items. |
| [ISyncMgrHandlerCollection::BindToHandler](..\syncmgr\nf-syncmgr-isyncmgrhandlercollection-bindtohandler.md) | Instantiates a specified sync handler when called by Sync Center. |
| [ISyncMgrHandlerCollection::GetHandlerEnumerator](..\syncmgr\nf-syncmgr-isyncmgrhandlercollection-gethandlerenumerator.md) | Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user. |
| [ISyncMgrHandlerInfo::GetComment](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-getcomment.md) | Gets a string that contains commentary regarding the handler. |
| [ISyncMgrHandlerInfo::GetLastSyncTime](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-getlastsynctime.md) | Gets the date and time when the handler was last synchronized. |
| [ISyncMgrHandlerInfo::GetTypeLabel](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-gettypelabel.md) | Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string. |
| [ISyncMgrHandlerInfo::GetType](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-gettype.md) | Gets the handler type for Sync Center. |
| [ISyncMgrHandlerInfo::IsActive](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-isactive.md) | Gets a value that indicates whether the handler can be synchronized. |
| [ISyncMgrHandlerInfo::IsConnected](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-isconnected.md) | Gets a value that indicates whether the handler&#8212;typically some type of external device&#8212;is connected. |
| [ISyncMgrHandlerInfo::IsEnabled](..\syncmgr\nf-syncmgr-isyncmgrhandlerinfo-isenabled.md) | Gets a value that indicates whether the handler is enabled. |
| [ISyncMgrRegister::GetHandlerRegistrationInfo](..\mobsync\nf-mobsync-isyncmgrregister-gethandlerregistrationinfo.md) | Called by the registered application's handler to get current registration information. |
| [ISyncMgrRegister::RegisterSyncMgrHandler](..\mobsync\nf-mobsync-isyncmgrregister-registersyncmgrhandler.md) | Registers a handler with the synchronization manager when the handler has items to synchronize. |
| [ISyncMgrRegister::UnregisterSyncMgrHandler](..\mobsync\nf-mobsync-isyncmgrregister-unregistersyncmgrhandler.md) | Removes a handler's class identifier (CLSID) from the registration. A handler should call this when it no longer has any items to synchronize. |
| [ISyncMgrResolutionHandler::KeepItems](..\syncmgr\nf-syncmgr-isyncmgrresolutionhandler-keepitems.md) | Keeps the Shell items that are passed in. |
| [ISyncMgrResolutionHandler::KeepOther](..\syncmgr\nf-syncmgr-isyncmgrresolutionhandler-keepother.md) | Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals. |
| [ISyncMgrResolutionHandler::KeepRecent](..\syncmgr\nf-syncmgr-isyncmgrresolutionhandler-keeprecent.md) | Keeps the more recent copy. |
| [ISyncMgrResolutionHandler::QueryAbilities](..\syncmgr\nf-syncmgr-isyncmgrresolutionhandler-queryabilities.md) | Determines what options the conflict presenter will display. |
| [ISyncMgrResolutionHandler::RemoveFromSyncSet](..\syncmgr\nf-syncmgr-isyncmgrresolutionhandler-removefromsyncset.md) | Deletes the conflict and removes the IShellItem from synchronization. |
| [ISyncMgrScheduleWizardUIOperation::InitWizard](..\syncmgr\nf-syncmgr-isyncmgrschedulewizarduioperation-initwizard.md) | Initializes the sync schedule wizard. |
| [ISyncMgrSessionCreator::CreateSession](..\syncmgr\nf-syncmgr-isyncmgrsessioncreator-createsession.md) | Notifies Sync Center that synchronization of the specified items has begun. |
| [ISyncMgrSyncCallback::AddItemToSession](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-additemtosession.md) | Adds a specified item to the set of items currently being synchronized. |
| [ISyncMgrSyncCallback::CanContinue](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-cancontinue.md) | Determines whether the synchronization has been canceled. |
| [ISyncMgrSyncCallback::CommitItem](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-commititem.md) | Confirms a specified item as a member of the handler's sync set and confirms that it should be shown in the UI. |
| [ISyncMgrSyncCallback::ProposeItem](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-proposeitem.md) | Proposes the addition of a new item to the set of items previously enumerated. |
| [ISyncMgrSyncCallback::QueryForAdditionalItems](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-queryforadditionalitems.md) | Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized after the current synchronization is finished. |
| [ISyncMgrSyncCallback::ReportEvent](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-reportevent.md) | Provides an event to add to the Sync Results folder for an item being synchronized. |
| [ISyncMgrSyncCallback::ReportManualSync](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-reportmanualsync.md) | Reports that a synchronization operation is being performed that was requested manually from outside the Sync Center UI. |
| [ISyncMgrSyncCallback::ReportProgress](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-reportprogress.md) | Reports the progress of the synchronization of a single sync item to Sync Center. |
| [ISyncMgrSyncCallback::SetHandlerProgressText](..\syncmgr\nf-syncmgr-isyncmgrsynccallback-sethandlerprogresstext.md) | Sets the content of an information field for the handler while that handler is performing a synchronization. |
| [ISyncMgrSyncItem::Delete](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-delete.md) | Deletes a sync item. |
| [ISyncMgrSyncItem::Enable](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-enable.md) | Enables or disables the sync item. |
| [ISyncMgrSyncItem::GetCapabilities](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getcapabilities.md) | Gets a set of flags describing the item's defined capabilities. |
| [ISyncMgrSyncItem::GetItemID](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getitemid.md) | Gets the unique ID of a sync item. |
| [ISyncMgrSyncItem::GetItemInfo](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getiteminfo.md) | Gets the properties of a sync item. |
| [ISyncMgrSyncItem::GetName](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getname.md) | Gets the UI display name of the sync item. |
| [ISyncMgrSyncItem::GetObject](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getobject.md) | Creates a specific type of object related to the item. |
| [ISyncMgrSyncItem::GetPolicies](..\syncmgr\nf-syncmgr-isyncmgrsyncitem-getpolicies.md) | Gets a set of flags describing the policies set by the item. |
| [ISyncMgrSyncItemContainer::GetSyncItemCount](..\syncmgr\nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount.md) | Gets a count of the sync items in the container. |
| [ISyncMgrSyncItemContainer::GetSyncItemEnumerator](..\syncmgr\nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator.md) | Gets an interface that enumerates the handler's sync items. |
| [ISyncMgrSyncItemContainer::GetSyncItem](..\syncmgr\nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem.md) | Gets a specified sync item. |
| [ISyncMgrSyncItemInfo::GetComment](..\syncmgr\nf-syncmgr-isyncmgrsynciteminfo-getcomment.md) | Gets a string that contains commentary regarding the item. |
| [ISyncMgrSyncItemInfo::GetLastSyncTime](..\syncmgr\nf-syncmgr-isyncmgrsynciteminfo-getlastsynctime.md) | Gets the date and time when the item was last synchronized. |
| [ISyncMgrSyncItemInfo::GetTypeLabel](..\syncmgr\nf-syncmgr-isyncmgrsynciteminfo-gettypelabel.md) | Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string. |
| [ISyncMgrSyncItemInfo::IsConnected](..\syncmgr\nf-syncmgr-isyncmgrsynciteminfo-isconnected.md) | Generates a value that indicates whether the item&#8212;typically some type of external device&#8212;is connected. |
| [ISyncMgrSyncItemInfo::IsEnabled](..\syncmgr\nf-syncmgr-isyncmgrsynciteminfo-isenabled.md) | Generates a value that indicates whether the item is enabled. |
| [ISyncMgrSyncResult::Result](..\syncmgr\nf-syncmgr-isyncmgrsyncresult-result.md) | Gets the result of a StartHandlerSync or StartItemSync call. |
| [ISyncMgrSynchronize::EnumSyncMgrItems](..\mobsync\nf-mobsync-isyncmgrsynchronize-enumsyncmgritems.md) | Obtains the ISyncMgrEnumItems interface for the items that are handled by a registered application. |
| [ISyncMgrSynchronize::GetHandlerInfo](..\mobsync\nf-mobsync-isyncmgrsynchronize-gethandlerinfo.md) | Obtains handler information. |
| [ISyncMgrSynchronize::GetItemObject](..\mobsync\nf-mobsync-isyncmgrsynchronize-getitemobject.md) | Obtains an interface on a specified item that a registered application handles. |
| [ISyncMgrSynchronize::Initialize](..\mobsync\nf-mobsync-isyncmgrsynchronize-initialize.md) | Called by the synchronization manager in a registered application handler to determine whether the handler processes the synchronization event. |
| [ISyncMgrSynchronize::PrepareForSync](..\mobsync\nf-mobsync-isyncmgrsynchronize-prepareforsync.md) | Allows a registered application to display any user interface, and perform any necessary initialization before the ISyncMgrSynchronize |
| [ISyncMgrSynchronize::SetItemStatus](..\mobsync\nf-mobsync-isyncmgrsynchronize-setitemstatus.md) | Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases |
| [ISyncMgrSynchronize::SetProgressCallback](..\mobsync\nf-mobsync-isyncmgrsynchronize-setprogresscallback.md) | Sets the ISyncMgrSynchronizeCallback interface. Registered applications use this callback interface to give status information from within the ISyncMgrSynchronize |
| [ISyncMgrSynchronize::ShowError](..\mobsync\nf-mobsync-isyncmgrsynchronize-showerror.md) | Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab. |
| [ISyncMgrSynchronize::ShowProperties](..\mobsync\nf-mobsync-isyncmgrsynchronize-showproperties.md) | Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the Properties button. |
| [ISyncMgrSynchronize::Synchronize](..\mobsync\nf-mobsync-isyncmgrsynchronize-synchronize.md) | Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized. |
| [ISyncMgrSynchronizeCallback::DeleteLogError](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-deletelogerror.md) | Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box. |
| [ISyncMgrSynchronizeCallback::EnableModeless](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-enablemodeless.md) | Called by the registered application before and after any dialog boxes are displayed from within the PrepareForSync and Synchronize methods. |
| [ISyncMgrSynchronizeCallback::EstablishConnection](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-establishconnection.md) | Called by the registered application's handler when a network connection is required. |
| [ISyncMgrSynchronizeCallback::LogError](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-logerror.md) | Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box. |
| [ISyncMgrSynchronizeCallback::PrepareForSyncCompleted](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted.md) | Called by a registered handler of an application after the PrepareForSync method is complete. |
| [ISyncMgrSynchronizeCallback::Progress](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-progress.md) | Called by a registered application to update the progress information and determine whether an operation should continue. |
| [ISyncMgrSynchronizeCallback::ShowErrorCompleted](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-showerrorcompleted.md) | Called by the registered application's handler before or after its PrepareForSync operation has been completed. |
| [ISyncMgrSynchronizeCallback::ShowPropertiesCompleted](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-showpropertiescompleted.md) | Called by the registered application's handler before or after its ShowProperties operation is completed. |
| [ISyncMgrSynchronizeCallback::SynchronizeCompleted](..\mobsync\nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted.md) | Called by an application when its Synchronize method is complete. |
| [ISyncMgrSynchronizeInvoke::UpdateAll](..\mobsync\nf-mobsync-isyncmgrsynchronizeinvoke-updateall.md) | Programmatically starts an update for all items. |
| [ISyncMgrSynchronizeInvoke::UpdateItems](..\mobsync\nf-mobsync-isyncmgrsynchronizeinvoke-updateitems.md) | Programmatically starts an update for specified items. |
| [ISyncMgrUIOperation::Run](..\syncmgr\nf-syncmgr-isyncmgruioperation-run.md) | Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center. |
| [IThumbnailCache::GetThumbnailByID](..\thumbcache\nf-thumbcache-ithumbnailcache-getthumbnailbyid.md) | Gets a thumbnail from the thumbnail cache, given its ID. |
| [IThumbnailCache::GetThumbnail](..\thumbcache\nf-thumbcache-ithumbnailcache-getthumbnail.md) | Gets a cached thumbnail for a given Shell item. |
| [IThumbnailProvider::GetThumbnail](..\thumbcache\nf-thumbcache-ithumbnailprovider-getthumbnail.md) | Gets a thumbnail image and alpha type. |
| [IThumbnailSettings::SetContext](..\thumbcache\nf-thumbcache-ithumbnailsettings-setcontext.md) | Enables a thumbnail provider to return a thumbnail specific to the user's context. |
| [IThumbnailStreamCache::GetThumbnailStream](..\thumbnailstreamcache\nf-thumbnailstreamcache-ithumbnailstreamcache-getthumbnailstream.md) | Gets the thumbnail stream. This method is for internal use only and can only be called by the photos application. |
| [IThumbnailStreamCache::SetThumbnailStream](..\thumbnailstreamcache\nf-thumbnailstreamcache-ithumbnailstreamcache-setthumbnailstream.md) | Sets the thumbnail stream. This method is for internal use only and can only be called by the photos application. |
| [ITrackShellMenu::Popup](..\shdeprecated\nf-shdeprecated-itrackshellmenu-popup.md) | Displays a modal pop-up menu at a specific location. |
| [ITrackShellMenu::SetObscured](..\shdeprecated\nf-shdeprecated-itrackshellmenu-setobscured.md) | Coordinates obscured items on a toolbar with items in a menu. |
| [ITranscodeImage::TranscodeImage](..\imagetranscode\nf-imagetranscode-itranscodeimage-transcodeimage.md) | Converts an image to JPEG or bitmap (BMP) image format. |
| [ITravelEntry::GetPidl](..\shdeprecated\nf-shdeprecated-itravelentry-getpidl.md) | Deprecated. Gets the pointer to an item identifier list (PIDL) associated with the travel entry. |
| [ITravelEntry::Invoke](..\shdeprecated\nf-shdeprecated-itravelentry-invoke.md) | Deprecated. Invokes the travel entry, navigating to that page. |
| [ITravelEntry::Update](..\shdeprecated\nf-shdeprecated-itravelentry-update.md) | Deprecated. Updates the travel entry. |
| [ITravelLog::AddEntry](..\shdeprecated\nf-shdeprecated-itravellog-addentry.md) | Deprecated. Adds a new entry for a pending navigation to the travel log. |
| [ITravelLog::Clone](..\shdeprecated\nf-shdeprecated-itravellog-clone.md) | Deprecated. Duplicates the contents of the current travel log. |
| [ITravelLog::CountEntries](..\shdeprecated\nf-shdeprecated-itravellog-countentries.md) | Deprecated. Generates the number of entries in the travel log. |
| [ITravelLog::FindTravelEntry](..\shdeprecated\nf-shdeprecated-itravellog-findtravelentry.md) | Deprecated. Determines whether a specific travel entry is present in the travel log. |
| [ITravelLog::GetToolTipText](..\shdeprecated\nf-shdeprecated-itravellog-gettooltiptext.md) | Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI. |
| [ITravelLog::GetTravelEntry](..\shdeprecated\nf-shdeprecated-itravellog-gettravelentry.md) | Deprecated. Gets a travel entry in the travel log relative to the position of the current entry. |
| [ITravelLog::InsertMenuEntries](..\shdeprecated\nf-shdeprecated-itravellog-insertmenuentries.md) | Deprecated. Inserts entries into the specified menu. |
| [ITravelLog::Revert](..\shdeprecated\nf-shdeprecated-itravellog-revert.md) | Deprecated. Reverts to the current entry, dropping the result of ITravelLog |
| [ITravelLog::Travel](..\shdeprecated\nf-shdeprecated-itravellog-travel.md) | Deprecated. Navigates to a travel entry in the travel log relative to the position of the current entry. |
| [ITravelLog::UpdateEntry](..\shdeprecated\nf-shdeprecated-itravellog-updateentry.md) | Deprecated. Saves the browser state of the current entry in preparation for a pending navigation. |
| [ITravelLog::UpdateExternal](..\shdeprecated\nf-shdeprecated-itravellog-updateexternal.md) | Deprecated. Updates an entry that originated out of the current procedure through IHlinkFrame. |
